# Personal VPN
## Shadowsocks+V2Ray-plugin

Click the button below to deploy, and remember to order a Star if it works:

(1): Select Repo on render.com
(2): Select Region, Enter AppName.
(3): Set The Following Variables In Environment Variables:
- AppName
- PASSWORD
- ENCRYPT
(4): If You Dont Know What To Enter In PASSWORD and ENCRYPT. Set Only AppName Environment Variable, Else Scroll Below This Readme to know more about the variables

## Variable Info

(1): ENCRYPT
- Description: Encryption method, due to https blessing, choose the simplest one, default: chacha20-ietf-poly1305, others are（aes-256-cfb,chacha20-ietf-poly1305,salsa20,chacha20-ietf etc.）

(2): PASSWORD
- Description: The password of shadowsocks, you can use uuid as the password (http://www.uuid.online/ online generation). default: 5c301bb8-6c77-41a0-a606-4ba11bbab084

## 0. Attention

Deployment requires registration of a render account, a email is required when registering a render account (otherwise the verification code cannot be brushed out). 

An email address that can receive verification codes normally (@qq.com, @163.com are not acceptable):
- gmail (Best) 
- Outlook <https://login.live.com/> here.

## 1. Verification

After the server is deployed, open app to display the webpage normally. After the address is filled with the path (for example: <https://test.onrender.com/static>), the 404 page is displayed, which means the deployment is successful.

## 2. Client Configuration

QR code address: https://test.onrender.com/qr_img/vpn.png

Use the client (Shadowsocks recommended) to scan the QR code.

**or**

Use Configuration file -> Address: https://test.onrender.com/qr_img/

(Change test to your own app name)

Copy the details after opening and import it to the client.

**or**

Manual configuration:

```sh
Server: test.onrender.com (change test to your app name)
Port: 443
Password: The password filled in during deployment
Encry Method: RC4-MD5 (or other methods you fill in)
Plugin: v2ray
Plugin Transport mode: websocket-tls
Hostname: Same as Server
Path: The path you filled in during deployment
```

Those without a client can also download from here (Android):

[shadowsocks](https://github.com/shadowsocks/shadowsocks-android/releases/latest/download/shadowsocks--universal-5.1.9.apk)

[v2ray-plugin](https://github.com/shadowsocks/v2ray-plugin-android/releases/latest/download/v2ray-arm64-v8a-1.3.1.apk)

windows:

<https://github.com/shadowsocks/shadowsocks-windows/wiki/Shadowsocks-Windows-%E4%BD%BF%E7%94%A8%E8%AF%B4%E6%98%8E>


# Reference

https://github.com/ygcaicn/ss-heroku

https://github.com/xiangrui120/v2ray-heroku-undone

https://hub.docker.com/r/shadowsocks/shadowsocks-libev

https://github.com/shadowsocks/v2ray-plugin
