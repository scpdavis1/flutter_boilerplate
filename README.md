# Set up flutter app

## Download flutter and dart sdk:
* The vscode extension can prompt you to download it. You can just open a new flutter project and itll ask.
    * extension: `https://marketplace.visualstudio.com/items?itemName=Dart-Code.flutter`
* Or manually download it:
	* Link to sdk: `https://docs.flutter.dev/install/manual`
	* What I did: I copied the linux sdk into /opt/ and vscode adds it to path for you. Im sure its the same on windows.

## Set up the basic project:
* Set up through Vscode:
    * `ctrl+shift+p`, then type in `"Flutter: New Project"`. Then follow its steps.
* Commandline Setup:
    * Go to your project directory.
    * Create command: `flutter create <app_name>`
    * There are more configurations you can set up if you want.

## Build/run the flutter app:
* Use one of these methods:
    * Vscode can do it all if you want it to. just click the run button on the top right of vscode while main.dart is highlighted.
    * Commandline Method:
        * Run `flutter run`. 
        * A flutter interface will start in the terminal and (probably) a desktop compiled version of the app will show up.
	* Commandline with other device: 
        * Run `flutter run -d <device>` 
        * Device should be another platform. For example, if you want edge or firefox put "web-server", if you want chrome put "chrome". Im sure there are other ways to connect other devices like a phone.
* If an error occurs, you're probably missing cmake or something. here is a list of dependencies I needed to get for on linux:
    * `curl git unzip xz-utils zip libglu1-mesa clang cmake ninja-build pkg-config libgtk-3-dev build-essential`
* Cleaning your build: `flutter clean`.
* Update flutter package using pub: `flutter pub get`

## Structure info:
* The "main file" in this empty project will be `<project>/lib/main.dart`.
