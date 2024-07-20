# Instagram React Native Project

An Instagram Clone App made using React Native. Easy to understand code pattern.

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

Here's a basic example of how to use the component:

- Each option is wrapped in a `TouchableOpacity` to make them clickable.


**Import necessary components from react-native.
Import the useState hook from react.**

import { View, Text, Image, TouchableOpacity, Modal } from 'react-native';
import React, { useState } from 'react';

const ProfileHeader = () => {
    // State to manage the visibility of the modal
    const [open, setOpen] = useState(false);

    // Function to toggle the modal visibility
    const handleModal = () => {
        setOpen(!open);
    };

const handleModal = () => {
        setOpen(!open);
    };
    return (
        <View style={{ paddingHorizontal: 15, paddingTop: 10, height: 55 }}>
            <View
                style={{
                    flexDirection: 'row',
                    justifyContent: 'space-between',
                    alignItems: 'center',
                }}>
                <Text style={{ fontSize: 24, fontWeight: '500', color: 'black' }}>
                    Kumar Harsh
                </Text>
                <View style={{ flexDirection: 'row', alignItems: 'center' }}>
                    <TouchableOpacity style={{ marginRight: 15 }}>
                        <Image
                            style={{ height: 24, width: 24 }}
                            source={require('../assets/footer/addPost.png')}
                        />
                    </TouchableOpacity>
                    <TouchableOpacity onPress={handleModal}>
                        <Image
                            style={{ height: 20, width: 20, tintColor: 'black' }}
                            source={require('../assets/icon/Menu.png')}
                        />
                    </TouchableOpacity>
                </View>
            </View>
            <Modal
                animationType="slide"
                transparent={true}
                visible={open}
                onRequestClose={() => {
                    setOpen(!open);
                }}>
                <View style={{ flex: 1, justifyContent: 'flex-end' }}>
                    <View
                        style={{
                            backgroundColor: '#ffffff',
                            height: 580,
                            borderTopEndRadius: 25,
                            borderTopStartRadius: 25,
                        }}>
                        <TouchableOpacity onPress={handleModal}>
                            <Image
                                style={{ alignSelf: 'center' }}
                                source={require('../assets/icon/Modalclose.png')}
                            />
                            <View style={{ paddingHorizontal: 20 }}>
                                <TouchableOpacity style={{ borderBottomWidth: 1 }}>
                                    <Text style={{ fontSize: 18, paddingVertical: 15 }}>
                                        Setting and privacy
                                    </Text>
                                </TouchableOpacity>
                                <TouchableOpacity style={{ borderBottomWidth: 1 }}>
                                    <Text style={{ fontSize: 18, paddingVertical: 15 }}>
                                        Your activity
                                    </Text>
                                </TouchableOpacity>
                                <TouchableOpacity style={{ borderBottomWidth: 1 }}>
                                    <Text style={{ fontSize: 18, paddingVertical: 15 }}>
                                        Archive
                                    </Text>
                                </TouchableOpacity>
                                <TouchableOpacity style={{ borderBottomWidth: 1 }}>
                                    <Text style={{ fontSize: 18, paddingVertical: 15 }}>Saved</Text>
                                </TouchableOpacity>
                                <TouchableOpacity style={{ borderBottomWidth: 1 }}>
                                    <Text style={{ fontSize: 18, paddingVertical: 15 }}>
                                        SuperVision
                                    </Text>
                                </TouchableOpacity>
                                <TouchableOpacity style={{ borderBottomWidth: 1 }}>
                                    <Text style={{ fontSize: 18, paddingVertical: 15 }}>
                                        Meta Varified
                                    </Text>
                                </TouchableOpacity>
                                <TouchableOpacity style={{ borderBottomWidth: 1 }}>
                                    <Text style={{ fontSize: 18, paddingVertical: 15 }}>
                                        Close Friends
                                    </Text>
                                </TouchableOpacity>
                                <TouchableOpacity style={{ borderBottomWidth: 1 }}>
                                    <Text style={{ fontSize: 18, paddingVertical: 15 }}>
                                        Favourites
                                    </Text>
                                </TouchableOpacity>
                            </View>
                        </TouchableOpacity>
                    </View>
                </View>
            </Modal>
        </View>
    );
};

export default ProfileHeader;
    
    




