# Fintoc: Create Link Intent

Creates a link intent in Fintoc.

```
POST https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/create-link-intent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fintoc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/create-link-intent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "product": "movements",
  "holderType": "individual",
  "country": "cl"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fintoc/latest/actions/create-link-intent', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "product": "movements",
    "holderType": "individual",
    "country": "cl"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `product` | string | yes | Product to request in the link intent (for example: movements). Example: `movements`. |
| `holderType` | string | yes | Holder type (for example: individual). Example: `individual`. |
| `country` | string | yes | ISO 3166-1 alpha-2 country code (for example: cl). Example: `cl`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country": "string",
      "created_at": "string",
      "exchange_token": "string",
      "exchange_token_expires_at": "string",
      "holder_type": "string",
      "id": "string",
      "mode": "string",
      "object": "string",
      "product": "string",
      "status": "string",
      "widget_token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string |  |
| `created_at` | string |  |
| `exchange_token` | string |  |
| `exchange_token_expires_at` | string |  |
| `holder_type` | string |  |
| `id` | string |  |
| `mode` | string |  |
| `object` | string |  |
| `product` | string |  |
| `status` | string |  |
| `widget_token` | string |  |

## Native endpoint

Through the native Fintoc API, this operation is `POST /v1/link_intents` (base URL `https://api.fintoc.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-link-intent.md) for the provider-specific parameters and requirements.

