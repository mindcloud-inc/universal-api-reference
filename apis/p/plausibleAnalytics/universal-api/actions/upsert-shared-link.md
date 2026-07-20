# Plausible Analytics: Upsert Shared Link

Finds or creates a shared dashboard link in Plausible Analytics.

```
PUT https://connect.mindcloud.co/v1/universal/plausibleAnalytics/latest/actions/upsert-shared-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Plausible Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/plausibleAnalytics/latest/actions/upsert-shared-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/plausibleAnalytics/latest/actions/upsert-shared-link', {
  method: 'PUT',
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
      "name": "Ava Chen",
      "siteId": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `siteId` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Plausible Analytics API, this operation is `PUT /api/v1/sites/shared-links` (base URL `https://plausible.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-shared-link.md) for the provider-specific parameters and requirements.

