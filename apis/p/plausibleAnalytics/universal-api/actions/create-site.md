# Plausible Analytics: Create Site

Creates a new site in Plausible Analytics.

```
POST https://connect.mindcloud.co/v1/universal/plausibleAnalytics/latest/actions/create-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Plausible Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/plausibleAnalytics/latest/actions/create-site" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/plausibleAnalytics/latest/actions/create-site', {
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
      "domain": "string",
      "id": "string",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domain` | string |  |
| `id` | string |  |
| `timezone` | string |  |

## Native endpoint

Through the native Plausible Analytics API, this operation is `POST /api/v1/sites` (base URL `https://plausible.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-site.md) for the provider-specific parameters and requirements.

