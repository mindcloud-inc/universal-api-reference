# SIGNL4: Get Alert Report

Retrieves an alert report from SIGNL4.

```
GET https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-alert-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SIGNL4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-alert-report?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-alert-report?${params}`, {
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
      "data": {
        "acknowledged": 1,
        "categoryCounts": [
          {}
        ],
        "closed": 1,
        "start": "2026-05-07T12:00:00.000Z",
        "subscriptionId": "string",
        "teamId": "string",
        "type": 1,
        "typeString": "string",
        "unhandled": 1
      },
      "errors": [
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
| `data` | array<object> |  |
| `data.acknowledged` | number |  |
| `data.categoryCounts` | array<object> |  |
| `data.closed` | number |  |
| `data.start` | date |  |
| `data.subscriptionId` | string |  |
| `data.teamId` | string |  |
| `data.type` | number |  |
| `data.typeString` | string |  |
| `data.unhandled` | number |  |
| `errors` | array<object> |  |

## Native endpoint

Through the native SIGNL4 API, this operation is `GET /v2/alerts/report` (base URL `https://connect.signl4.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-alert-report.md) for the provider-specific parameters and requirements.

