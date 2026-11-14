# Daily Dozen Tracker

**An iOS and Apple Watch app that makes daily nutrition tracking a one-tap habit.** Built as my senior capstone in Computer Science at Occidental College (2025–2026).

Most health-tracking apps get abandoned because logging takes too many steps. This app tracks Dr. Michael Greger's "Daily Dozen" checklist (beans, berries, greens, whole grains, and more) and moves logging out of the app and onto the surfaces people already look at: the Home Screen, the Lock Screen, and the Apple Watch.

![Apple Watch complication](watchimage%281%29.JPG)

## Features

- **Interactive Home Screen widget:** log a serving with a single tap, without opening the app
- **Lock Screen widget:** see daily progress at a glance
- **Apple Watch complication:** a progress ring showing how much of the Daily Dozen is done
- **Shared data across app, widgets, and watch** via App Groups

## Results

I ran a comparative task analysis and a qualitative user study with 8 participants:

- Widgets cut the number of steps to log a serving by **66%** compared with the in-app flow
- Every participant said checking progress "at a glance" felt easier than opening the app

The full write-up is in [`completedRevisedFinal.tex`](completedRevisedFinal.tex).

## Tech

- Swift 5, SwiftUI
- WidgetKit (Home Screen, Lock Screen, and watchOS complications)
- App Intents (background logging from the widget)
- App Groups (shared state between the app, widget extension, and watch)

## Running it

Requires a Mac with Xcode 15+ and an iOS 17 device or simulator (interactive widgets need iOS 17).

1. Clone the repo and open the `.xcodeproj` in `DailyDozenTracker/`
2. Under **Signing & Capabilities**, pick your development team for both the app target and the widget extension target
3. Build and run the `DailyDozenTracker` scheme on a simulator (iPhone 15 Pro works well)
4. On the simulator's Home Screen, long-press, tap **+**, search "DailyDozen", and add the widget
