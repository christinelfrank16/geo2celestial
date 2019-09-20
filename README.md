# Geo2Celestial

#### Converts geological coordinates to celestial coordinates, 20-Sept-2019

#### By **Christine Frank**

## Description

This application provides the user celestial coordinates of right ascension and declination based on the input of geographical coordinates of latitude and longitude and date-time. Resulting output for right ascension is provided in hours, and for declination, in units of degrees. The input of date-time is optional; with no input, the current date-time is used.

## Install
```
$ npm install geo2celestial
```

## Usage
```
import { Geo2Celestial } from 'geo2celestial';

\\ No date time input: default uses current date-time
const geoCoords = new Geo2Celestial(50.23,-136.45);

const celestialRA = geoCoords.rightAscension();
const celestialDec = geoCoords.declination();

```

Or for specific date time:
```
import { Geo2Celestial } from 'geo2celestial';

const dateTime = new Date('December 17, 1995 03:24:00');
const geoCoords = new Geo2Celestial(50.23,-136.45, dateTime);

const celestialRA = geoCoords.rightAscension();
const celestialDec = geoCoords.declination();

```
## To Dos
- [x] Add date time input option
- [ ] Provide functions to separate GMST, GAST, LMST, LAST
- [ ] Account for nutation in declination calculations
- [ ] Update to allow view angle besides zenith (straight up)

## Issues?
Create a issue in the GitHub repo!
https://github.com/christinelfrank16/geo2celestial

### License

*This application is licensed under the MIT license*

Copyright (c) 2019 **_Christine Frank_**
