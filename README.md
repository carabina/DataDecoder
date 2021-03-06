# DataDecoder
Swift Data Decoder.  Easily Decode Data values

[![CI Status](http://img.shields.io/travis/FitnessKit/DataDecoder.svg?style=flat)](https://travis-ci.org/FitnessKit/DataDecoder)
[![Version](https://img.shields.io/cocoapods/v/DataDecoder.svg?style=flat)](http://cocoapods.org/pods/DataDecoder)
[![License](https://img.shields.io/cocoapods/l/DataDecoder.svg?style=flat)](http://cocoapods.org/pods/DataDecoder)
[![Platform](https://img.shields.io/cocoapods/p/DataDecoder.svg?style=flat)](http://cocoapods.org/pods/DataDecoder)

## Installation

DataDecoder is available through [CocoaPods](http://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod "DataDecoder"
```


## How to Use ##

~~~
  let sensorData: Data = Data([ 0x02, 0xFE, 0xFF, 0xEF, 0xBE, 0xAD, 0xDE, 0xA5])

  var decoder = DataDecoder(sensorData)
  let height = decoder.decodeUInt8()
  let weight = decoder.decodeUInt16()
  let deadbeef = decoder.decodeUInt32()
  let nib = decoder.decodeNibble()
  let novalue = decoder.decodeNibble() //This should come back 0 as there is no more data  left
  ~~~

## Data Decoders ##

* Nibble
* UInt8/Int8
* UInt16/Int16
* UInt24/Int23
* UInt32/Int32
* UInt48
* UInt64/Int64
* IEEE-11073 16-bit SFLOAT
* IEEE-11073 32-bit FLOAT
* IP Address to String Value
* MAC Address to String Value

## Author

Kevin A. Hoogheem, kevin@hoogheem.net

## License

DataDecoder is available under the MIT license. See the LICENSE file for more info.
