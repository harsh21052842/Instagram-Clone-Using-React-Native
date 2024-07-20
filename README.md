# Instagram React Native Project

An Instagram Clone App made using React Native.

## Features
- Shows stories
- Supports multiple accounts
- Displays likes and comments
- Includes a profile section
- User login with credentials

## Prerequisites
- Node.js
- React Native CLI
- JavaScript
- Basic CSS

## Installation

1. **Clone the repository**
    ```bash
    gh repo clone harsh21052842/Instagram-Clone-Using-React-Native
    cd Instagram-Clone-Using-React-Native
    ```

2. **Install dependencies**
    ```bash
    npm install
    ```

3. **Run the app**
    ```bash
    npm start
    ```

    For iOS:
    ```bash
    npx react-native run-ios
    ```

    For Android:
    ```bash
    npx react-native run-android
    ```

## Usage

Here's a basic example of how to use the Instagram Feed component:

```javascript
import React from 'react';
import { InstagramFeed } from './InstagramFeed';

const App = () => {
  return (
    <InstagramFeed />
  );
};

export default App;
