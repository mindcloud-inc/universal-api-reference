# CallTrackingMetrics: Get Webhook Details

Retrieves detailed webhook information from CallTrackingMetrics.

```
GET https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/get-webhook-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallTrackingMetrics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/get-webhook-details?connectionId=$CONNECTION_ID&webhookId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "webhookId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/get-webhook-details?${params}`, {
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
| `webhookId` | string | yes | The CallTrackingMetrics webhook ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "clientId": 1,
      "clientType": "string",
      "id": 1,
      "name": "Ava Chen",
      "position": "string",
      "webhookConditions": [
        [
          "string"
        ]
      ],
      "weburl": "https://example.com",
      "withResourceUrl": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `clientId` | number |  |
| `clientType` | string |  |
| `id` | number |  |
| `name` | string |  |
| `position` | string |  |
| `webhookConditions[]` | array |  |
| `weburl` | string |  |
| `withResourceUrl` | boolean |  |

## Native endpoint

Through the native CallTrackingMetrics API, this operation is `GET /accounts/:accountId/webhooks/:webhookId` (base URL `https://api.calltrackingmetrics.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-webhook-details.md) for the provider-specific parameters and requirements.

