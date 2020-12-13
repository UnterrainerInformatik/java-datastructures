![GitHub forks](https://img.shields.io/github/forks/UnterrainerInformatik/java-datastructures?style=social) ![GitHub stars](https://img.shields.io/github/stars/UnterrainerInformatik/java-datastructures?style=social) ![GitHub repo size](https://img.shields.io/github/repo-size/UnterrainerInformatik/java-datastructures) [![GitHub issues](https://img.shields.io/github/issues/UnterrainerInformatik/java-datastructures)](https://github.com/UnterrainerInformatik/java-datastructures/issues)

[![license](https://img.shields.io/github/license/unterrainerinformatik/FiniteStateMachine.svg?maxAge=2592000)](http://unlicense.org) [![Travis-build](https://travis-ci.org/UnterrainerInformatik/java-datastructures.svg?branch=master)](https://travis-ci.org/github/UnterrainerInformatik/java-datastructures) [![Maven Central](https://img.shields.io/maven-central/v/info.unterrainer.commons/datastructures)](https://search.maven.org/artifact/info.unterrainer.commons/datastructures) [![Twitter Follow](https://img.shields.io/twitter/follow/throbax.svg?style=social&label=Follow&maxAge=2592000)](https://twitter.com/throbax)



# datastructures

A library that contains various data-structures.



## Tuple2

This class is a simple generic implementation of a two-tuple.



## Interval

Is exactly what the name suggests. An interval defined by a minimum and a maximum with getters and setters implementing several safety-mechanisms like automatic boundary adaption when changing them, etc...



## Fader

The fader consists of an interval and adds a value (double) to it. The value is always in between the interval.  
It adds a percentage getter and setter as well allowing you to do conversions from a percentage-value to your interval and backwards.



# Remarks

All of our projects facilitate the [Project Lombok][lombok]. So please download it and 'install' it in your preferred IDE by clicking on the downloaded jar-file. Then all compile-errors should vanish.  
We use the following parts of Project Lombok.

This program is brought to you by [Unterrainer Informatik][homepage].



[homepage]:  https://unterrainer.info
[lombok]: https://projectlombok.org

