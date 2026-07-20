# Leadberry: Disable Website



```
PUT https://connect.mindcloud.co/v1/universal/leadberry/latest/actions/disable-website
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadberry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/leadberry/latest/actions/disable-website" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leadberry/latest/actions/disable-website', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dataProviderId` | string | no |  |
| `isp` | string | no |  |
| `token` | string | no |  |
| `type` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Leadberry API returns.

## Native endpoint

Through the native Leadberry API, this operation is `POST /data/disableSite` (base URL `https://app.leadberry.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/disable-website.md) for the provider-specific parameters and requirements.

