![Logo](admin/rct.png)
# ioBroker.rct

[![NPM version](https://img.shields.io/npm/v/iobroker.rct.svg)](https://www.npmjs.com/package/iobroker.rct)
[![Downloads](https://img.shields.io/npm/dm/iobroker.rct.svg)](https://www.npmjs.com/package/iobroker.rct)
![Number of Installations (latest)](https://iobroker.live/badges/rct-installed.svg)
![Number of Installations (stable)](https://iobroker.live/badges/rct-stable.svg)
[![Dependency Status](https://img.shields.io/david/lauff/iobroker.rct.svg)](https://david-dm.org/lauff/iobroker.rct)

[![NPM](https://nodei.co/npm/iobroker.rct.png?downloads=true)](https://nodei.co/npm/iobroker.rct/)

**Tests:** ![Test and Release](https://github.com/lauff/ioBroker.rct/workflows/Test%20and%20Release/badge.svg)

## RCT adapter for ioBroker

Show values of a RCT Power photovolatics power converter

## REMARKS

### Early Pre-Release

Please not that this is a very early pre-release with very limited functionality.

Configuration is still limited and rather technical. Using the "RCT ELemente" it can be selected which data shall be read from the power converter. Default is "battery.soc,battery.soc_target,battery.soc_target_low,battery.soc_target_high,dc_conv.dc_conv_struct[0].p_dc_lp,dc_conv.dc_conv_struct[1].p_dc_lp,g_sync.p_ac_grid_sum_lp,g_sync.p_acc_lp,g_sync.p_ac_load_sum_lp". Other elements can be found in the code (file "rct/rc_core.js"). But this is not self descriptive at all (even not really tested).

### Known Issues

As for now, it is not clear how the RCT power connector handles multiple parallel connections. Because of that, connecting to the power converter from multiple sources causes unpredicted behaviour. This typically also means that accessing the power converter from the mobile RCT app will disconnect the ioBroker adapter. 

## Changelog

### 0.0.5
* (Markus Lauff) some fixes / minor improvements
### 0.0.1
* (Markus Lauff) initially bare minimum working release

## License
MIT License

Copyright (c) 2021: Markus Lauff <rct@markus.lauff.com>

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.