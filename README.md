
# React Native Cards 

![npm version](https://img.shields.io/npm/v/react-native-cards.svg?style=flat-square) ![npm downloads](https://img.shields.io/npm/dm/react-native-cards.svg?style=flat-square) ![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)

### A highly customizable material design card component for React Native.

See [Google Material Design](https://material.io/guidelines/components/cards.html) for more info on Cards.

![Images](https://image.ibb.co/jdxsEG/screenshots.png)

## Get Started

### Installation

Install using npm:
```
npm install --save react-native-cards
```
or install using Yarn
```
yarn add react-native-cards
```

## Basic Usage

Import the components like so:  
```javascript
import { Card, CardTitle, CardContent, CardAction, CardButton, CardImage } from 'react-native-cards';
```

Then insert the card in your code:
```js
<ScrollView>

  <Card>
    <CardImage 
      source={{uri: 'http://bit.ly/2GfzooV'}} 
      title="Top 10 South African beaches"
    />
    <CardTitle
      subtitle="Number 6"
    />
    <CardContent text="Clifton, Western Cape" />
    <CardAction 
      separator={true} 
      inColumn={false}>
      <CardButton
        onPress={() => {}}
        title="Share"
        color="#FEB557"
      />
      <CardButton
        onPress={() => {}}
        title="Explore"
        color="#FEB557"
      />
    </CardAction>
  </Card>

</ScrollView>
```

## Card Component Options
| Prop        | Type           | Effect  | Default Value |
| ------------- |-------------| -----| -----|
| `isDark` | `boolean` | If the card background is dark, sets a light text color, this prop is passed to all child components | `true` |
| `mediaSource` | `object` | The image to show in background of a card, with content overlayed, passed to Image's `source` prop | `undefined` |
| `avatarSource` | `object` | The avatar image to be shown in the card's content or header section, whichever comes first, passed to Image's `source` prop | `undefined` |
| `style` | `object` | The style object to be merged with the default style | `undefined` |

## CardTitle Component Options
| Prop        | Type           | Effect  | Default Value |
| ------------- |-------------| -----| -----|
| `title` | `string` | The title text | `undefined` |
| `subtitle` | `string` | The subtitle text | `undefined` |
| `subtitleAbove` | `boolean` | Whether the subtitle should be shown above the title | `false` |
| `avatarSource` | `object` | The avatar image to be shown, passed to Image's `source` prop | `undefined` |
| `style` | `object` | The style object to be merged with the default style | `undefined` |

## CardContent Component Options
| Prop        | Type           | Effect  | Default Value |
| ------------- |-------------| -----| -----|
| `text` | `string` | The content text | `undefined` |
| `avatarSource` | `object` | The avatar image to be shown, passed to Image's `source` prop | `undefined` |
| `style` | `object` | The style object to be merged with the default style | `undefined` |

## CardImage Component Options
| Prop        | Type           | Effect  | Default Value |
| ------------- |-------------| -----| -----|
| `source` | `object` | The image to be shown, passed to Image's `source` prop | `undefined` |
| `style` | `object` | The style object to be merged with the default style | `undefined` |
| `resizeMode` | `string` | Determines how to resize the image when the frame doesn't match the raw image dimensions | `cover` |
| `resizeMethod` | `string` | Resize the image when the image's dimensions differ from the image view's dimensions. | `resize` |

## CardAction Component Options
| Prop        | Type           | Effect  | Default Value |
| ------------- |-------------| -----| -----|
| `separator` | `boolean` | Whether a separator should be shown | `true` |
| `inColumn` | `boolean` | Whether the buttons should be stacked in a column | `false` |
| `style` | `object` | The style object to be merged with the default style | `undefined` |

## CardButton Component Options
| Prop        | Type           | Effect  | Default Value |
| ------------- |-------------| -----| -----|
| `title` | `string` | The button's text | `undefined` |
| `color` | `string` | The color of button text | `orange` |
| `onPress` | `function` | The function to be called when button is pressed | `noop` (defined in [`src/utils`](https://github.com/SiDevesh/React-Native-Material-Cards/blob/master/src/utils/index.js)) |
| `style` | `object` | The style object to be merged with the default style | `undefined` |

### Todo (PRs welcome!)
- [ ] Add side media to cards - see [here](https://material.io/guidelines/components/cards.html#cards-usage)
