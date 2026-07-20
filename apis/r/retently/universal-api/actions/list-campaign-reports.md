# Retently: List Campaign Reports

Retrieves a list of campaign reports from Retently.

```
GET https://connect.mindcloud.co/v1/universal/retently/latest/actions/list-campaign-reports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Retently `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/retently/latest/actions/list-campaign-reports?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/retently/latest/actions/list-campaign-reports?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignId": "string",
      "channel": "string",
      "deliveryStats": {},
      "isActive": true,
      "last": {},
      "metric": "string",
      "name": "Ava Chen",
      "questionsStats": [
        "string"
      ],
      "trend": [
        "string"
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignId` | string |  |
| `channel` | string |  |
| `deliveryStats` | object |  |
| `isActive` | boolean |  |
| `last` | object |  |
| `metric` | string |  |
| `name` | string |  |
| `questionsStats` | array<string> |  |
| `trend` | array<string> |  |
| `type` | string |  |

## Native endpoint

Through the native Retently API, this operation is `GET /api/v2/reports` (base URL `https://app.retently.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-campaign-reports.md) for the provider-specific parameters and requirements.

