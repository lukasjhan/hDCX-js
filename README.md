# hDCX

Simplest Wallet Core SDK for Typescript

With just simple interfaces, you can significantly simplify the credential managing logic in you project. And it also covered in all aspects of speed, robustness, security and privacy to help you build a better experience.

- Fast and lightweight credential managing
- Simple interfaces, easy to understand and use
- Developer friendly, typed and clear error messages

---

<!-- View full documentation on [here]() -->

## Quick Start

### Wallet initialization
```ts
// Initialize wallet
const wallet = new Wallet();
```
### Recieve and save credentials
```ts
// You get the url or data for issued credentials
const issuePayload = await scanQRCode(); // or deeplink or NFC/BLE

// The library will recognize the method and will get it for you
const credentials = await wallet.receive(issuePayload);

// Then you can save credentials
await wallet.save(credentials)
```
### Load and present credentials
```ts
// Load credentials with query
const credentials = await wallet.load(['name', 'age']);

// Present Credentials
const presentation = await wallet.present(credentials);
```

![img](/assets/wallet.png)

## Interoperability

We are interoperable with

| Name        | Interoperable |
| ----------- | ------------- |
| Lissi       | ⌛            |
| Amino Funke | ⌛            |

## License

MIT
