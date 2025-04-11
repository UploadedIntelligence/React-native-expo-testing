This repo is the result of following the steps, but you have to run `npm install` to get everything if you want to just work from this repo, otherwise follow the next steps if you want to generate your own environment.

extensions(optional for VScode):
React Native Tools(by Microsoft) - debug reactive native apps in VScode
React-Native/React/Redux(by EQuimper) - helps with code generation

mandatory steps for initialization of a new expo/react-native environment:
-npx create-expo-app NameOfApp(or test) --template - create expo project, choose Blank(TypeScript) for our current project
-Change directory to the newly created folder (NameOfApp(or test))
-npx expo start - this will give you an url and a QR code, you can use them in your app(look at next step) in order to view the website you're working on
-Download "Expo Go" app on your phone and either enter the url manually or scan the QR code


Xcode - iOS emulator if you have a mac device, windows devices can't use it

https://developer.android.com/studio
Android Studio - emulation of Android environment for testing.
ctrl+n (or m) for developer options

Important distinctions between react-native and regular react components:

When doing styling, we don't have a css file which points at the tags' classes or ids, instead we have a prop called `style` which then needs to refer to a utility object called `StyleSheet`.
Example:
`const styles = StyleSheet.create({
  text: {
    fontSize: 20,
    color: 'red',
  },
});`
In this case if we want to apply the styles we have to use the `style` prop in our component like so:
`<Text style={styles.text}>Hello World!</Text>`
Our variable styles is treated like an object and each key/value pair represents a style that we can apply through it.
For more detailed information on the various styling that can be applied to each component read here:
https://reactnative.dev/docs/stylesheet
