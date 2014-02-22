# Getting Started With Phonegap For iOS

### In short: 

Open Terminal and do the following: 

1. `npm i -g phonegap`
2. `phonegap create hello com.example.hello HelloWorld`
3. `phonegap build ios`

To run the app in the iOS emulator: 

    phonegap run ios

**Note:** The `run` command will do `build` for you, but if you don't want to instantly run the app in the simulator then use `build` separately.

If the iOS simulator node module isn't installed already (it's probably not), then you will need to install it. This is supposed to be automatic, but my copy of Phonegap threw an error for some reason. I this happens just install it manually: 

    npm i -g ios-sim

**The documentation for Phonegap is seriously out of date, and it doesn't ever seem to distinguish between Cordova and Phonegap in a meaningful way.**

The info on [this page][more_docs] is decent for getting started:

[more_docs]: http://docs.phonegap.com/en/edge/guide_cli_index.md.html#The%20Command-Line%20Interface

### Running on an iPhone or iPad (With a Developer Account)

Make sure you're iPhone or iPad is connected via USB and then run: 

    phonegap run ios --device

This, as with deploying to the simulator is supposed to work automatically out of the box but it also gave me problems when trying to install the necessary dependency, ios-deploy. If you get errors, as above just install manually: 

    npm i -g ios-deploy

Now you should be able to run your app on iOS :)

**Note:** For the above to work you do need to have an Apple developer account and have already set up your devices for development... or just follow the instructions bellow.

### Running on a Jailbroken Device without a Developer Account

1. Install AppSync through Cydia. Your jailbroken device should already have Cydia, but in Cydia you probably don't have access to AppSync by default. You will need to add an external Cydia repo that has AppSync. Add one of the repos from [this page on installing AppSync][repos].
2. Download and install [Jailcoder][jailcoder].
3. Open Jailcoder and hit the big button to do a guided install.

That's all, now you can enjoy testing apps on a real device without the need for an apple developer account. That being said, if you want to publish your apps to the App Store you will need a developer account. But $99 per year is probably well worth it if you're going to be publishing apps. Enjoy1

[jailcoder]: http://oneiros.altervista.org/jailcoder/
[repos]: http://www.cydiasources.net/appsync-repo-source.html
