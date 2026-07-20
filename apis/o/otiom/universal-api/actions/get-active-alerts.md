# Otiom: Get Active Alerts

Retrieves active alerts from Otiom.

```
GET https://connect.mindcloud.co/v1/universal/otiom/latest/actions/get-active-alerts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Otiom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/otiom/latest/actions/get-active-alerts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/otiom/latest/actions/get-active-alerts?${params}`, {
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
      "alerts": [
        {
          "active": true,
          "alertId": 1,
          "body": "string",
          "infoUrl": "https://example.com",
          "severity": 1
        }
      ],
      "updateChannels": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alerts[].active` | boolean |  |
| `alerts[].alertId` | number |  |
| `alerts[].body` | string |  |
| `alerts[].infoUrl` | string |  |
| `alerts[].severity` | number |  |
| `updateChannels[]` | string |  |

## Native endpoint

Through the native Otiom API, this operation is `GET /api/alerts/active` (base URL `https://api.otiom.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-active-alerts.md) for the provider-specific parameters and requirements.

