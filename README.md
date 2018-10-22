# WiaTagKit
WiaTagKit is a library that will help developers to build communication with Wialon platform using WiaTag binary protocol.

## Installation
- Add .jar file to your project.
- Declare the following permission in your Android Manifest file: 
```
<uses-permission android:name="android.permission.INTERNET" />
```

## Example
First you need to  initialise MessageSender with host, port, unitId and password:
```
MessageSender.initWithHost("193.193.165.165",20963,"123456","unitpassword");
```
After initialisation is done you may prepare message you want to send:
```
Message message = new Message().time((int)((new Date()).getTime()/1000)).Sos();
```
and send it:
```
MessageSender.sendMessage(message, new MessageSenderListener() {
        @Override
        protected void onSuccess() {
            super.onSuccess();
        }
        @Override
        protected void onFailure(final byte errorCode) {
            super.onFailure(errorCode);
        }
    });
```


## Author

Gurtam, development@gurtam.com

## License

WiaTagKit is available under the CC BY-ND 4.0 license. See the LICENSE file for more info.

## Installation



### Todos

 - Write detailed Example
 - Add project to Maven


