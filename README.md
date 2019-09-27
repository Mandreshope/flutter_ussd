# ussd
[![pub package](https://img.shields.io/pub/v/wave.svg?style=flat-square)](https://pub.dev/packages/ussd) ![GitHub](https://img.shields.io/github/license/mashape/apistatus.svg?longCache=true&style=flat-square)

Run ussd code directly in your application

## Getting Started

``` Dart

import 'package:flutter/material.dart';
import 'dart:async';

import 'package:ussd/ussd.dart';

void main() => runApp(MyApp());

class MyApp extends StatefulWidget {
  @override
  _MyAppState createState() => _MyAppState();
}

class _MyAppState extends State<MyApp> {

  @override
  void initState() {
    super.initState();
  }

  Future<void> launchUssd(String ussdCode) async {
    Ussd.runUssd(ussdCode);
  }

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(
          title: const Text('Run ussd code plugin by mandreshope'),
        ),
        body: Center(
          child: Column(
            children: <Widget>[
              RaisedButton(
                onPressed: () {
                  launchUssd("#123#");
                }, 
                child: Text("Tap to run ussd Orange Mg operator"),
              ),
              RaisedButton(
                onPressed: () {
                  launchUssd("*999#");
                }, 
                child: Text("Tap to run ussd Airtel Mg operator"),
              ),
            ],
          )
        ),
      ),
    );
  }
}

```
