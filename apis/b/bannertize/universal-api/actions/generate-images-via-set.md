# Bannertize: Generate Images via Set

Creates multiple images from a set in Bannertize.

```
POST https://connect.mindcloud.co/v1/universal/bannertize/latest/actions/generate-images-via-set
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bannertize `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bannertize/latest/actions/generate-images-via-set" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "set": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bannertize/latest/actions/generate-images-via-set', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "set": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `modifications[]` | array<object> | no | An array of Bannertize layer modifications to apply to the set. |
| `set` | string | yes | The Bannertize set UID to render. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Bannertize API returns.

## Native endpoint

Through the native Bannertize API, this operation is `POST set` (base URL `https://api.bannertize.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-images-via-set.md) for the provider-specific parameters and requirements.

