# Privy: Get Intent

Retrieves an intent from Privy by ID.

```
GET https://connect.mindcloud.co/v1/universal/privy/latest/actions/get-intent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Privy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/privy/latest/actions/get-intent?connectionId=$CONNECTION_ID&intentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "intentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/privy/latest/actions/get-intent?${params}`, {
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
| `intentId` | string | yes | Privy intent ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action_result": {},
      "current_resource_data": {
        "address": "string",
        "id": "string"
      },
      "intent_type": "string",
      "request_details": {
        "body": {
          "wallet_id": "string"
        },
        "method": "string",
        "url": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action_result` | object |  |
| `current_resource_data.address` | string |  |
| `current_resource_data.id` | string |  |
| `intent_type` | string |  |
| `request_details.body.wallet_id` | string |  |
| `request_details.method` | string |  |
| `request_details.url` | string |  |

## Native endpoint

Through the native Privy API, this operation is `GET /v1/intents/{{intentId}}` (base URL `https://api.privy.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-intent.md) for the provider-specific parameters and requirements.

