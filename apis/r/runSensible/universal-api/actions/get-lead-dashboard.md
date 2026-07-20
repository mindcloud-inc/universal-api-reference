# RunSensible: Get Lead Dashboard



```
GET https://connect.mindcloud.co/v1/universal/runSensible/latest/actions/get-lead-dashboard
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RunSensible `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runSensible/latest/actions/get-lead-dashboard?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/runSensible/latest/actions/get-lead-dashboard?${params}`, {
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
      "inProgress": 1,
      "qualified": 1,
      "total": 1,
      "unqualified": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `inProgress` | number |  |
| `qualified` | number |  |
| `total` | number |  |
| `unqualified` | number |  |

## Native endpoint

Through the native RunSensible API, this operation is `GET /api/Report/GetLeadDashboard` (base URL `https://app.runsensible.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-lead-dashboard.md) for the provider-specific parameters and requirements.

