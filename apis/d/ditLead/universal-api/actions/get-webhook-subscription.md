# DitLead: Get Webhook Subscription



```
GET https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/get-webhook-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DitLead `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/get-webhook-subscription?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/get-webhook-subscription?${params}`, {
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
| `subscriptionId` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": [
        "string"
      ],
      "eventId": [
        "string"
      ],
      "success": true,
      "updatedAt": [
        "string"
      ],
      "url": [
        "https://example.com"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | array<string> |  |
| `eventId` | array<string> |  |
| `success` | boolean |  |
| `updatedAt` | array<string> |  |
| `url` | array<string> |  |

## Native endpoint

Through the native DitLead API, this operation is `GET /v1/webhook` (base URL `https://api.ditlead.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook-subscription.md) for the provider-specific parameters and requirements.

