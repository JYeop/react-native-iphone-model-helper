# react-native-iphone-model-helper

Helps you to identify the device model and the screen ratio.

### Elements

- getDeviceModel: Returns a string of the device model name.

```js
import { getDeviceModel } from "react-native-iphone-model-helper";

console.log(getDeviceModel());
// >> 'iPhone XS Max'
```

- isIphone{model}: Returns a boolean.
  - Supporting models: "XS, XS Max, XR, X, 8, 8 Plus, 7, 7 Plus, SE, 6, 6 Plus, 5s, 5c
  - Function names:
    isIphoneX,
    isIphoneXs,
    isIphoneXsMax,
    isIphoneXr,
    isIphone8,
    isIphone8Plus,
    isIphone7,
    isIphone7Plus,
    isIphoneSe,
    isIphone6,
    isIphone6Plus,
    isIphone5s,
    isIphone5c

```js
import { isIphoneXsMax } from "react-native-iphone-model-helper";

console.log(isIphoneXsMax());
// if the model is 'iphone xs max':
// >> true
// else:
// >> false
```

- wr: Returns a number calculated with the ratio of the device width. You can import this with 'widthByRatio'.

```js
import { StyleSheet } from "react-native";
import { wr, widthByRatio } from "react-native-responsive-percent";

export default StyleSheet.create({
  image: {
    width: wr(0.15) // On iphoneX : 56, iphoneXS Max: 62
    // width: wr('0.15')   // Same above
    // width: widthByRatio(15)   // Same above
  }
});
```

- hp: Returns a number calculated with the ratio of the device height. You can import this with 'heightByPercent'.

```js
import { StyleSheet } from "react-native";
import { hp, heightByPercent } from "react-native-responsive-percent";

export default StyleSheet.create({
  image: {
    height: hp(15) // On iphoneX : 121, iphoneXS Max: 134
    // height: hp('15%')   // Same above
    // height: hp('15')   // Same above
    // width: heightByPercent(15)   // Same above
  }
});
```

- hr: Returns a number calculated with the ratio of the device height. You can import this with 'heightByRatio'.

```js
import { StyleSheet } from "react-native";
import { hr, heightByRatio } from "react-native-responsive-percent";

export default StyleSheet.create({
  image: {
    height: hr(0.15) // On iphoneX : 121, iphoneXS Max: 134
    // height: hr('0.15')   // Same above
    // width: heightByRatio(15)   // Same above
  }
});
```

#### Example

```js
import { StyleSheet } from "react-native";
import RNRP from "react-native-responsive-percent";

export default StyleSheet.create({
  title: {
    fontSize: RNRP.f(15)
  }
});
```
