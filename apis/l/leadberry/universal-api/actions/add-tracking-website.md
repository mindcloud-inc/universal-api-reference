# Leadberry: Add Tracking Website



```
POST https://connect.mindcloud.co/v1/universal/leadberry/latest/actions/add-tracking-website
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadberry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/leadberry/latest/actions/add-tracking-website" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leadberry/latest/actions/add-tracking-website', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | Website URL to add for Leadberry tracking. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Leadberry API returns.

## Native endpoint

Through the native Leadberry API, this operation is `POST /data/addTrackingWebsite` (base URL `https://app.leadberry.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-tracking-website.md) for the provider-specific parameters and requirements.

