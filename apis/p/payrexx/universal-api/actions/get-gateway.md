# Payrexx: Get Gateway

Retrieves a gateway from Payrexx.

```
GET https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/get-gateway
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Payrexx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/get-gateway?connectionId=$CONNECTION_ID&id=32603338" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "32603338"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/get-gateway?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | ID of gateway payment to retrieve. Example: `32603338`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "applicationFee": 1,
      "createdAt": 1,
      "currency": "string",
      "hash": "string",
      "id": 1,
      "language": "string",
      "link": "https://example.com",
      "preAuthorization": true,
      "referenceId": "string",
      "sku": {},
      "status": "string",
      "vatRate": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `applicationFee` | number |  |
| `createdAt` | number |  |
| `currency` | string |  |
| `hash` | string |  |
| `id` | number |  |
| `language` | string |  |
| `link` | string |  |
| `preAuthorization` | boolean |  |
| `referenceId` | string |  |
| `sku` | object |  |
| `status` | string |  |
| `vatRate` | number |  |

## Native endpoint

Through the native Payrexx API, this operation is `GET Gateway/:id/` (base URL `https://api.payrexx.com/v1.14/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-gateway.md) for the provider-specific parameters and requirements.

