# F12018UDP

[![Build Status](https://travis-ci.org/irvingswiftj/f1-2018-udp.svg?branch=master)](https://travis-ci.org/irvingswiftj/f1-2018-udp)

A javascript UDP client for Codemaster's F1 2018 game

## Get started

### Turn on UDP in F1 2018

Goto the Telemetry section from the settings panel

![alt text](https://raw.githubusercontent.com/irvingswiftj/f1-2018-udp/master/docs/screenshot_1.jpg "Settings Page")

Enable Telemetry. Settings that I have working are as below (Screenshot from PS4, may differ on PC/Xbox)

![alt text](https://raw.githubusercontent.com/irvingswiftj/f1-2018-udp/master/docs/screenshot_2.jpg "Telemetry Settings Page")

### Install this module

yarn:
```
yarn add f1-2018-udp
```

npm:
```
npm install f1-2018-udp
```

### How to use this module

```js
import { F12018UDP } from 'f1-2018-udp';
// const F12018UDP = require('f1-2018-udp').default;

const client = new F12018UDP();
client.on('SESSION', m => console.log(m));
client.on('MOTION', m => console.log(m));

//the following listeners need implementing:
client.on('LAP_DATA', m => console.log(m);
client.on('EVENT', m => console.log(m);
client.on('PARTICIPENTS', m => console.log(m);
client.on('CAR_SETUPS', m => console.log(m);
client.on('CAR_TELEMETRY', m => console.log(m);
client.on('CAR_STATUS', m => console.log(m);
client.on('PACKET_TYPES', m => console.log(m);


// to start listening:
client.start();

// and when you want to stop:
client.stop();
```

## TODO

- Write Tests!
- Add Parsers according to documentation: https://forums.codemasters.com/discussion/136948/f1-2018-udp-specification