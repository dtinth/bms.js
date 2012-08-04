bms.js
======

`BMS.parse(bms string)`
--
Parse BMS data and returns a JavaScript object.


`BMS.stringify(bms object)`
--
Generate BMS data from BMS object.


`BMS.isNote(event object)`
--
Checks if the event object is a note event. (11-29, 51,69)

BMS Object
--
    { "headers": { ... }
    , "keysounds": { ... }
    , "measureSizes": { "0": 0.5 }
    , "events": [ bms events... ]
    }

BMS Event Object
--
    { "measure": measure number (5 for #005)
    , "position": position in measure (0 through 1)
    , "channel": bms channel (see below)
    , "value": "ZZ" (number for BPM events, string for others)
    }

For BPM events, only use channel=8. BPM events gets normalized during parsing and when stringified will
be converted to hex-bpm or ref-bpm automatically.








