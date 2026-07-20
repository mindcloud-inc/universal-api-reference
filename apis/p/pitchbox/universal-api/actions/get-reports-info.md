# Pitchbox: Get Reports Info



```
GET https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/get-reports-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pitchbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/get-reports-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pitchbox/latest/actions/get-reports-info?${params}`, {
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
      "campaignCount": 1,
      "campaignsOverTime": [
        {}
      ],
      "outreachOverTime": [
        {}
      ],
      "respondedCount": 1,
      "responsesByAttempt": [
        {}
      ],
      "sentCount": 1,
      "wonCount": 1,
      "wonLostOverTime": [
        {}
      ],
      "workflowOverTime": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignCount` | number |  |
| `campaignsOverTime` | array<object> |  |
| `outreachOverTime` | array<object> |  |
| `respondedCount` | number |  |
| `responsesByAttempt` | array<object> |  |
| `sentCount` | number |  |
| `wonCount` | number |  |
| `wonLostOverTime` | array<object> |  |
| `workflowOverTime` | array<object> |  |

## Native endpoint

Through the native Pitchbox API, this operation is `GET /api/reports` (base URL `https://apiv2.pitchbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-reports-info.md) for the provider-specific parameters and requirements.

