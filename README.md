# 🍋 acho

Acho is a Swift library to generate interactive CLI prompts.

**Where does acho come from?** People from Murcia, the region where I'm from use acho a lot when speaking. It's a word that can be used for many things: grab someone's attention, ask or complain about something, tell someone not to do something anymore. Since I found a parallelism between one of the usages of the expression, and the goal of this library, asking the user for something, I thought it'd be the perfect name for the library.

![CircleCI branch](https://img.shields.io/circleci/project/github/tuist/acho/master.svg)
![Swift Package Manager](https://img.shields.io/badge/swift%20package%20manager-compatible-brightgreen.svg)
![Release](https://img.shields.io/github/release/tuist/acho.svg)
![Code Coverage](https://codecov.io/gh/xcodeswift/xcproj/branch/master/graph/badge.svg)
![Slack](http://slack.tuist.io/badge.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)
[![Say Thanks!](https://img.shields.io/badge/Say%20Thanks-!-1EAEDB.svg)](https://saythanks.io/to/pepibumur)
<img src="https://opencollective.com/tuistapp/tiers/backer/badge.svg?label=backer&color=brightgreen" />
<img src="https://opencollective.com/tuistapp/tiers/sponsor/badge.svg?label=sponsor&color=brightgreen" />
[![Join the community on Spectrum](https://withspectrum.github.io/badge/badge.svg)](https://spectrum.chat/tuist)

## Install 🛠

### Swift Package Manager

Add the dependency in your `Package.swift` file:

```swift
let package = Package(
    name: "myproject",
    dependencies: [
        .package(url: "https://github.com/tuist/acho.git", .upToNextMajor(from: "6.2.0")),
        ],
    targets: [
        .target(
            name: "myproject",
            dependencies: ["acho"]),
        ]
)
```

## Usage 🚀

Create an instance of `Acho` passing the question and the options. The options need to conform both the protocol `CustomStringConvertible` and `Hashable`:

```swift
let simulators = ["iPhone 10", "iPhone 7" ]
let acho = Acho(question: "In which simulator would you like to run the app?",
                items: simulators)
let simulator = acho.ask()
```

![gif](assets/acho.gif)

## Setup for development 👩‍💻

1.  Git clone: `git@github.com:tuist/acho.git`
2.  Generate Xcode project with `swift package generate-xcodeproj`.
3.  Open `acho.xcodeproj`.
4.  Have fun 🤖

## Open source

Tuist is a proud supporter of the [Software Freedom Conservacy](https://sfconservancy.org/)

<a href="https://sfconservancy.org/supporter/"><img src="https://sfconservancy.org/img/supporter-badge.png" width="194" height="90" alt="Become a Conservancy Supporter!" border="0"/></a>
