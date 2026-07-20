# DataForB2B: Add Profiles To Monitor

Adds profiles to monitoring in DataForB2B.

```
PUT https://connect.mindcloud.co/v1/universal/dataForB2B/latest/actions/add-profiles-to-monitor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataForB2B `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dataForB2B/latest/actions/add-profiles-to-monitor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "profileIds": [
    "https://www.linkedin.com/in/satyanadella/"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dataForB2B/latest/actions/add-profiles-to-monitor', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "profileIds": ["https://www.linkedin.com/in/satyanadella/"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `profileIds` | object<string> | yes | Profile URLs or profile IDs to start monitoring. Default: `["https://www.linkedin.com/in/satyanadella/"]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "added": 1,
      "already_monitored": 1,
      "errors": [
        {}
      ],
      "failed": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `added` | number |  |
| `already_monitored` | number |  |
| `errors` | array<object> |  |
| `failed` | number |  |

## Native endpoint

Through the native DataForB2B API, this operation is `POST /webhooks/profiles` (base URL `https://api.dataforb2b.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-profiles-to-monitor.md) for the provider-specific parameters and requirements.

