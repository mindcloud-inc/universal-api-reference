# Anvil: Native API Reference

A consolidated summary of Anvil's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://www.useanvil.com/docs/api/graphql/reference/
- **API base URL:** `https://graphql.useanvil.com`

## Authentication

### Basic Auth

Provide your Anvil API key as the username. Anvil accepts any non-empty placeholder password when using HTTP Basic authentication.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://www.useanvil.com/docs/api/getting-started/#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Cast](actions/create-cast.md) | `POST /` | [docs](https://www.useanvil.com/docs/api/graphql/reference/#mutation-createCast) |
| [Create Etch Packet](actions/create-etch-packet.md) | `POST /` | [docs](https://www.useanvil.com/docs/api/graphql/reference/#mutation-createEtchPacket) |
| [Create Forge](actions/create-forge.md) | `POST /` | [docs](https://www.useanvil.com/docs/api/graphql/reference/#mutation-createForge) |
| [Create Submission](actions/create-submission.md) | `POST /` | [docs](https://www.useanvil.com/docs/api/graphql/reference/#mutation-createSubmission) |
| [Create Webhook](actions/create-webhook.md) | `POST /` | [docs](https://www.useanvil.com/docs/api/graphql/reference/#mutation-createWebhook) |
| [Create Webhook Action](actions/create-webhook-action.md) | `POST /` | [docs](https://www.useanvil.com/docs/api/graphql/reference/#mutation-createWebhookAction) |
| [Create Weld](actions/create-weld.md) | `POST /` | [docs](https://www.useanvil.com/docs/api/graphql/reference/#mutation-createWeld) |
| [Create Weld Data](actions/create-weld-data.md) | `POST /` | [docs](https://www.useanvil.com/docs/api/graphql/reference/#mutation-createWeldData) |
| [Expire Signer Tokens](actions/expire-signer-tokens.md) | `POST /` | [docs](https://www.useanvil.com/docs/api/graphql/reference/#mutation-expireSignerTokens) |
| [Generate Etch Sign URL](actions/generate-etch-sign-url.md) | `POST /` | [docs](https://www.useanvil.com/docs/api/graphql/reference/#mutation-generateEtchSignURL) |
| [Get Cast](actions/get-cast.md) | `POST /` | [docs](https://www.useanvil.com/docs/api/graphql/reference/#query-cast) |
| [Get Current User](actions/get-current-user.md) | `POST /` | [docs](https://www.useanvil.com/docs/api/graphql/reference/#query-currentUser) |
| [Get Etch Packet](actions/get-etch-packet.md) | `POST /` | [docs](https://www.useanvil.com/docs/api/graphql/reference/#query-etchPacket) |
| [Get Forge](actions/get-forge.md) | `POST /` | [docs](https://www.useanvil.com/docs/api/graphql/reference/#query-forge) |
| [Get Organization](actions/get-organization.md) | `POST /` | [docs](https://www.useanvil.com/docs/api/graphql/reference/#query-organization) |
| [Get Signer](actions/get-signer.md) | `POST /` | [docs](https://www.useanvil.com/docs/api/graphql/reference/#query-signer) |
| [Get Submission](actions/get-submission.md) | `POST /` | [docs](https://www.useanvil.com/docs/api/graphql/reference/#query-submission) |
| [Get Webhook Log](actions/get-webhook-log.md) | `POST /` | [docs](https://www.useanvil.com/docs/api/graphql/reference/#query-webhookLog) |
| [Get Weld](actions/get-weld.md) | `POST /` | [docs](https://www.useanvil.com/docs/api/graphql/reference/#query-weld) |
| [Get Weld Data](actions/get-weld-data.md) | `POST /` | [docs](https://www.useanvil.com/docs/api/graphql/reference/#query-weldData) |
| [Notify Signer](actions/notify-signer.md) | `POST /` | [docs](https://www.useanvil.com/docs/api/graphql/reference/#mutation-notifySigner) |
| [Publish Cast](actions/publish-cast.md) | `POST /` | [docs](https://www.useanvil.com/docs/api/graphql/reference/#mutation-publishCast) |
| [Publish Weld](actions/publish-weld.md) | `POST /` | [docs](https://www.useanvil.com/docs/api/graphql/reference/#mutation-publishWeld) |
| [Remove Etch Packet](actions/remove-etch-packet.md) | `POST /` | [docs](https://www.useanvil.com/docs/api/graphql/reference/#mutation-removeEtchPacket) |
| [Remove Webhook](actions/remove-webhook.md) | `POST /` | [docs](https://www.useanvil.com/docs/api/graphql/reference/#mutation-removeWebhook) |
| [Remove Webhook Action](actions/remove-webhook-action.md) | `POST /` | [docs](https://www.useanvil.com/docs/api/graphql/reference/#mutation-removeWebhookAction) |
| [Remove Weld Data](actions/remove-weld-data.md) | `POST /` | [docs](https://www.useanvil.com/docs/api/graphql/reference/#mutation-removeWeldData) |
| [Send Etch Packet](actions/send-etch-packet.md) | `POST /` | [docs](https://www.useanvil.com/docs/api/graphql/reference/#mutation-sendEtchPacket) |
| [Skip Signer](actions/skip-signer.md) | `POST /` | [docs](https://www.useanvil.com/docs/api/graphql/reference/#mutation-skipSigner) |
| [Submit Forge](actions/submit-forge.md) | `POST /` | [docs](https://www.useanvil.com/docs/api/graphql/reference/#mutation-forgeSubmit) |
| [Update Cast](actions/update-cast.md) | `POST /` | [docs](https://www.useanvil.com/docs/api/graphql/reference/#mutation-updateCast) |
| [Update Etch Packet](actions/update-etch-packet.md) | `POST /` | [docs](https://www.useanvil.com/docs/api/graphql/reference/#mutation-updateEtchPacket) |
| [Update Forge](actions/update-forge.md) | `POST /` | [docs](https://www.useanvil.com/docs/api/graphql/reference/#mutation-updateForge) |
| [Update Organization](actions/update-organization.md) | `POST /` | [docs](https://www.useanvil.com/docs/api/graphql/reference/#mutation-updateOrganization) |
| [Update Signer](actions/update-signer.md) | `POST /` | [docs](https://www.useanvil.com/docs/api/graphql/reference/#mutation-updateSigner) |
| [Update Submission](actions/update-submission.md) | `POST /` | [docs](https://www.useanvil.com/docs/api/graphql/reference/#mutation-updateSubmission) |
| [Update Webhook](actions/update-webhook.md) | `POST /` | [docs](https://www.useanvil.com/docs/api/graphql/reference/#mutation-updateWebhook) |
| [Update Weld](actions/update-weld.md) | `POST /` | [docs](https://www.useanvil.com/docs/api/graphql/reference/#mutation-updateWeld) |
| [Update Weld Data](actions/update-weld-data.md) | `POST /` | [docs](https://www.useanvil.com/docs/api/graphql/reference/#mutation-updateWeldData) |
| [Void Document Group](actions/void-document-group.md) | `POST /` | [docs](https://www.useanvil.com/docs/api/graphql/reference/#mutation-voidDocumentGroup) |
