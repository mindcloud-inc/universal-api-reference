# Headless Testing: Create Codeless Suite

Creates a codeless suite in Headless Testing.

```
POST https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/create-codeless-suite
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Headless Testing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/create-codeless-suite" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/create-codeless-suite', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "cron": "string",
      "id": 1,
      "name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cron` | string |  |
| `id` | number |  |
| `name` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Headless Testing API, this operation is `POST /labsuites` (base URL `https://api.testingbot.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-codeless-suite.md) for the provider-specific parameters and requirements.

