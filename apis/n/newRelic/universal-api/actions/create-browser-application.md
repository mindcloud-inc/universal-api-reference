# New Relic: Create Browser Application

Creates a new browser application in New Relic.

```
POST https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/create-browser-application
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a New Relic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/create-browser-application" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/create-browser-application', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Browser application name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "browser_application": {
        "browser_monitoring_key": "string",
        "id": 1,
        "loader_script": "string",
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `browser_application.browser_monitoring_key` | string |  |
| `browser_application.id` | number |  |
| `browser_application.loader_script` | string |  |
| `browser_application.name` | string |  |

## Native endpoint

Through the native New Relic API, this operation is `POST /browser_applications.json` (base URL `https://api.newrelic.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-browser-application.md) for the provider-specific parameters and requirements.

