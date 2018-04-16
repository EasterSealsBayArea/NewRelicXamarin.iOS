# NewRelic dll for SC iOS
NewRelic Xamarin binding for SC iOS

Instructions for iOS:

1. Checkout NewRelicXamarin.iOS from https://github.com/lnpquang/NewRelicXamarin.iOS.

2. Open terminal, go to NewRelicXamarin.iOS folder and run command: make 
After build process is completed. A NewRelicXamarin.iOS.dll is created in NewRelicXamarin.iOS project folder

3. Open SC solution, add reference to NewRelicXamarin.iOS.dll file in ESSC.iOS. 

4. Open file config.json in ESSC project, update value of "newrelicToken" variable.

5. Build and run ESSC app.
