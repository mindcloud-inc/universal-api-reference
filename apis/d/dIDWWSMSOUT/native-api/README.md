# DIDWW SMS OUT: Native API Reference

A consolidated summary of DIDWW SMS OUT's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://doc.didww.com/sms/sms-trunks/technical-data/http-specification.html
- **API base URL:** `https://us.sms-out.didww.com`

## Authentication

### HTTP OUT Basic Auth

Use the DIDWW SMS OUT trunk username and password from the HTTP OUT configuration screen.

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

[Official authentication documentation](https://doc.didww.com/sms/sms-trunks/technical-data/http-specification.html)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.api+json` |
| `Content-Type` | `application/vnd.api+json` |

Responses from this API use JSON. Response data is read from `data`.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Send Bulk SMS With Campaign](actions/send-bulk-sms-with-campaign.md) | `POST /bulk_outbound_messages` | [docs](https://doc.didww.com/sms/sms-trunks/technical-data/http-specification.html#outbound-sms-examples) |
| [Send Bulk SMS With Source](actions/send-bulk-sms-with-source.md) | `POST /bulk_outbound_messages` | [docs](https://doc.didww.com/sms/sms-trunks/technical-data/http-specification.html#outbound-sms-examples) |
| [Send SMS With Campaign](actions/send-sms-with-campaign.md) | `POST /outbound_messages` | [docs](https://doc.didww.com/sms/sms-trunks/technical-data/http-specification.html#outbound-sms-examples) |
| [Send SMS With Source](actions/send-sms-with-source.md) | `POST /outbound_messages` | [docs](https://doc.didww.com/sms/sms-trunks/technical-data/http-specification.html#outbound-sms-examples) |
