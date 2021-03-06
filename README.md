# <img src="http://sparse.tech/icons/trail.svg" width="50%">
[![Build Status](https://travis-ci.org/sparsetech/trail.svg)](https://travis-ci.org/sparsetech/trail)
[![Join the chat at https://gitter.im/sparsetech/trail](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/sparsetech/trail?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
[![Maven Central](https://img.shields.io/maven-central/v/tech.sparse/trail_2.13.svg)](http://search.maven.org/#search%7Cga%7C1%7Cg%3A%22tech.sparse%22%20AND%20a%3A%22trail_2.13%22)

Trail is a routing library for Scala. It is available for the JVM, Scala.js and Scala Native.

## Features
* Define type-safe routes
* Parse and generate URLs
* DSL to extract path elements, arguments and fragments
* Express routing tables via pattern matching
* Define custom codecs
* IDE support
* Cross-platform support (JVM, Scala.js, Scala Native)
* Zero dependencies

## Example
```scala
import trail._

val details  = Root / "details" / Arg[Int]
val userInfo = Root / "user" / Arg[String] & Param[Boolean]("show")

val result = "/user/hello?show=false" match {
  case details (a)      => s"details: $a"
  case userInfo((u, s)) => s"user: $u, show: $s"
}
```

## Links
* [Documentation](http://sparse.tech/docs/trail.html)
* [ScalaDoc](https://www.javadoc.io/doc/tech.sparse/trail_2.13/)

## Licence
Trail is licensed under the terms of the Apache v2.0 licence.

## Authors
* Tim Nieradzik
* Darren Gibson
* Anatolii Kmetiuk
