# New Relic: List Browser Applications

Retrieves browser applications from New Relic.

```
GET https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/list-browser-applications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a New Relic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/list-browser-applications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/list-browser-applications?${params}`, {
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
      "browser_applications": [
        {
          "browser_monitoring_key": "string",
          "id": 1,
          "loader_script": "string",
          "name": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `browser_applications[].browser_monitoring_key` | string |  |
| `browser_applications[].id` | number |  |
| `browser_applications[].loader_script` | string |  |
| `browser_applications[].name` | string |  |

## Native endpoint

Through the native New Relic API, this operation is `GET /browser_applications.json` (base URL `https://api.newrelic.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-browser-applications.md) for the provider-specific parameters and requirements.

