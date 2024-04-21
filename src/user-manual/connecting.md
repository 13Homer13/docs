# Connecting To Your Server

**Contents**

- [Connecting Locally](#connecting-locally)
- [Connecting with Your Router VPN](#connecting-with-your-router-vpn)
- [Connecting over Tor](#connecting-over-tor)

## Connecting Locally

To connect locally, you must be connected to the same LAN as your server. Local connections are the fastest possible, as they do not reach out to the Internet.

**Prerequisite**

- [Trusting Your Root CA](./trust-ca.md)

### Using .local (preferred)

Visit your server's unique `https://<adjective-noun>.local` address from any browser.

### Using IP

Visit your server's unique IP address from any browser. You can find your server's IP address in StartOS under `System > About`, or in your router settings.

```admonish danger title="Important - Set a Static IP"

Your router may unexpectedly change your server's IP address. To prevent this, assign a static IP address to your server in your router settings. This is supported by all routers. Refer to your router's user manual for instructions
```

## Connecting with Your Router VPN

**Prerequisite**

- [Trusting Your Root CA](./trust-ca.md)

Most modern routers have VPN functionality built-in. Refer to your router's user manual for instructions to complete the following steps.

1. Assign a static IP address to your server.

2. Enable your router's VPN.

   ```admonish tip title="Enable Dynamic DNS (Optional)"

   Rarely, your ISP may unexpectedly change your home IP address. If this happens, it will break your VPN connection until you re-complete the steps below. To prevent this, you can enable Dynamic DNS in your router, which is usually a paid service. To learn more about Dynamic DNS, click [here]().
   ```

3. Download your VPN config file from your router.

4. Install OpenVPN on your client device(s) and establish a VPN connection to your LAN using the config file from above.

## Connecting over Tor

```admonish warning

It is normal for Tor connections to be slow or unreliable at times.
```

You can connect to your server from anywhere in the world, privately and anonymously, by visiting its unique `http://....onion` URL from any Tor-enabled browser.

**Recommended Browsers**

- Linux, Mac, Windows, Android/Graphene: <a href="https://torproject.org/download" target="_blank">Tor Browser</a>
- iOS: <a href="https://onionbrowser.com" target="_blank">Onion Browser</a>
