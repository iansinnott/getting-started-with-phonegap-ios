# Getting Started With Phonegap For iOS

### In short: 

1. `npm i -g phonegap`
2. `phonegap create hello com.example.hello HelloWorld`
3. `phonegap build ios`

To run the app in the iOS emulator: 

1. `phonegap run ios`

**Note:** The run command will do `build` for you, but if you don't want to instantly run the app in the simulator then use `build` separately.

If the ios simulator node module isn't installed already (it's probably not), then you will need to install it. This is supposed to be automatic, but my copy of phonegap threw an error for some reason. I this happens just install it manually: 

    npm i -g ios-sim

#### The documentation for phonegap is seriously out of date, and it doesn't ever seem to distinguish between cordova and phonegap in a meaningful way.

The info on [this page][more_docs] is decent for getting started:

[more_docs]: http://docs.phonegap.com/en/edge/guide_cli_index.md.html#The%20Command-Line%20Interface

### Running on an iPhone/iPad

Make sure you're phone or ipad is connected via USB and then run: 

    phonegap run ios --device

This, as with deploying to the simulator is supposed to work automatically out of the tox but it also gave me problems when trying to install the necessary dependency, ios-deploy. If you get errors, as above just install manually: 

    npm i -g ios-deploy

Now you should be able to run your app on iOS :)
