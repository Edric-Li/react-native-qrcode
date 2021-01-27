# react-native-qrcode
React 生成二维码
***
[中文](https://github.com/Shealtiel-Li/react-native-qrcode/blob/master/README_CN.md)  | [English](https://github.com/Shealtiel-Li/react-native-qrcode/blob/master/README.md)
## 安装
```sh
npm install @p2m/react-native-qrcode --save
```
## 用法
```jsx
'use strict';

import React, { Component } from 'react'
import QRCode from 'react-native-qrcode';

import {
    AppRegistry,
    StyleSheet,
    View,
    TextInput
} from 'react-native';

class HelloWorld extends Component {
  state = {
    text: 'http://facebook.github.io/react-native/',
  };

  render() {
    return (
      <View style={styles.container}>
        <TextInput
          style={styles.input}
          onChangeText={(text) => this.setState({text: text})}
          value={this.state.text}
        />
        <QRCode
          value={this.state.text}
          size={200}
          bgColor='purple'
          fgColor='white'/>
      </View>
    );
  };
}

const styles = StyleSheet.create({
    container: {
        flex: 1,
        backgroundColor: 'white',
        alignItems: 'center',
        justifyContent: 'center'
    },

    input: {
        height: 40,
        borderColor: 'gray',
        borderWidth: 1,
        margin: 10,
        borderRadius: 5,
        padding: 5,
    }
});

AppRegistry.registerComponent('HelloWorld', () => HelloWorld);

module.exports = HelloWorld;
```
## Props

名称       | 类型                 | 默认值
----------|----------------------|--------------
`value`   | `string`             | `http://facebook.github.io/react-native/`
`size`    | `number`             | `128`
`bgColor` | `string` (CSS color) | `"#000"`
`fgColor` | `string` (CSS color) | `"#FFF"`
`style` | `object`               | `{opcity:0}`

# 许可证
所有源代码都是在 [MIT License](https://github.com/Shealtiel-Li/react-native-qrcode/blob/master/LICENSE).
