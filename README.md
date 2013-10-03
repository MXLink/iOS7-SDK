EstimoteSDK for iOS 7
=======

Overview
---------

Estimote SDK is a wrapper around Apple's CoreLocation framework. It is dedicated for iOS 7 as it's based on newly introduced CoreLocation framework functionality called iBeacon. It consists of 3 classes: ESTBeaconManager, ESTBeaconRegion and ESTBeacon. Each of them is an equivalent of CoreLocation classes (CLLocationManager, CLBeaconRegion, CLBeacon) created in particular for Estimate Beacons Platform.

ESTBeaconManager is a starting point of the library. It allows to get list of all estimate beacon devices (represented by ESTBeacon objects). It expose monitoring and ranging methods in the similar fashion then CLLocationManager. In addition to location functionality it allows to get list of beacons based CoreBluetooth framework. It is extremely important to have this option in case that device stop advertising in an iBeacon manner.

ESTBeaconRegion is a directly extending CLBeaconRegion class of CoreLocation framework. As Estimote Beacon Platform is using single ProximityUUID, this class helps create region object faster. You don't need to remember and play with ProximityUUID parameter.

ESTBeacon represents single beacon device. Objects of this class are generated using ESTBeaconManager (There is no sense to create them manually). The most important difference (comparing to CLBeacon class) is two way communication with the beacon device. Keeping reference to original CLBeacon object it allows to connect with the device and interact with it. All available bluetooth characteristics (like signal power or major/minor value) can be read and changed to create customised behaviour. Firmware update option is available using this class as well. 


Installation
---------