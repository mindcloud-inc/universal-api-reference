# RICOH360 Tours: Store Media Asset



```
POST https://connect.mindcloud.co/v1/universal/rICOH360Tours/latest/actions/store-media-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RICOH360 Tours `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rICOH360Tours/latest/actions/store-media-asset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rICOH360Tours/latest/actions/store-media-asset', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bucket` | string | no | Storage bucket for the asset. |
| `key` | string | no | Storage object key for the asset. |
| `region` | string | no | Storage region for the asset. |
| `url` | string | no | Source file URL to store. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native RICOH360 Tours API returns.

## Native endpoint

Through the native RICOH360 Tours API, this operation is `POST /graphql` (base URL `https://bbomwcm27nhalfwjvwzy6qbrim.appsync-api.us-west-2.amazonaws.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/store-media-asset.md) for the provider-specific parameters and requirements.

