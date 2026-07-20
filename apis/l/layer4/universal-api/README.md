# <img src="https://images.mindcloud.co/apps/icons/layer4_1776088192832.png" alt="Layer4 logo" width="28" height="28"> Layer4: Universal API

Create tokens, manage wallets, and store immutable records

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/layer4/latest
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.layer4.app/
- **Vendor API docs:** https://www.layer4.app/api-docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Wallets](actions/list-wallets.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/layer4/latest/actions/list-wallets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Record

| Action | Method | Description |
| --- | --- | --- |
| [Create Record](actions/create-record.md) | POST | Creates a new record in a Layer4 bucket. |
| [Get Record](actions/get-record.md) | GET | Retrieves a record from a Layer4 bucket. |
| [List Records](actions/list-records.md) | GET | Retrieves records from a Layer4 bucket. |

### Record Request

| Action | Method | Description |
| --- | --- | --- |
| [Async Create Record](actions/async-create-record.md) | POST | Creates a new record asynchronously in a Layer4 bucket. |
| [Get Record Request](actions/get-record-request.md) | GET | Retrieves a record request from a Layer4 bucket. |

### Recordrequest

| Action | Method | Description |
| --- | --- | --- |
| [List Record Requests](actions/list-record-requests.md) | GET | Retrieves record requests from a Layer4 bucket. |

### Token

| Action | Method | Description |
| --- | --- | --- |
| [Create Token](actions/create-token.md) | POST | Creates a new token in a Layer4 bucket. |
| [Get Token](actions/get-token.md) | GET | Retrieves a token from a Layer4 bucket. |
| [List Tokens](actions/list-tokens.md) | GET | Retrieves tokens from a Layer4 bucket. |

### Tokenmetadata

| Action | Method | Description |
| --- | --- | --- |
| [Get Token Metadata](actions/get-token-metadata.md) | GET | Retrieves the metadata of a Layer4 token. |

### Tokenrequest

| Action | Method | Description |
| --- | --- | --- |
| [Get Token Request](actions/get-token-request.md) | GET | Retrieves a token request from a Layer4 bucket. |
| [List Token Requests](actions/list-token-requests.md) | GET | Retrieves token requests from a Layer4 bucket. |

### Tokensupply

| Action | Method | Description |
| --- | --- | --- |
| [Get Token Supply](actions/get-token-supply.md) | GET | Retrieves the supply of a Layer4 token. |

### Wallet

| Action | Method | Description |
| --- | --- | --- |
| [List Wallets](actions/list-wallets.md) | GET | Retrieves wallets from Layer4. |

