# Abyssale: Create Dynamic Image URL

Creates a dynamic image URL in Abyssale.

```
POST https://connect.mindcloud.co/v1/universal/abyssale/latest/actions/create-dynamic-image-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Abyssale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/abyssale/latest/actions/create-dynamic-image-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "designId": "64238d01-d402-474b-8c2d-fbc957e9d290"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/abyssale/latest/actions/create-dynamic-image-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "designId": "64238d01-d402-474b-8c2d-fbc957e9d290"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `designId` | string | yes | Design ID associated with this dynamic image Example: `64238d01-d402-474b-8c2d-fbc957e9d290`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Abyssale API returns.

## Native endpoint

Through the native Abyssale API, this operation is `POST /designs/:designId/dynamic-image-url` (base URL `https://api.abyssale.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-dynamic-image-url.md) for the provider-specific parameters and requirements.

