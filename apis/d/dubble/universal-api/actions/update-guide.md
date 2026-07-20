# Dubble: Update Guide

Updates an existing guide in Dubble.

```
PUT https://connect.mindcloud.co/v1/universal/dubble/latest/actions/update-guide
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dubble `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dubble/latest/actions/update-guide" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "guideId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dubble/latest/actions/update-guide', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "guideId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `guideId` | string | yes | The ID of the guide |
| `title` | string | no | The title of the guide |
| `visibility` | string | no | The visibility setting for the guide |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dubble API returns.

## Native endpoint

Through the native Dubble API, this operation is `PUT /guides/:guideId` (base URL `https://api.dubble.so/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-guide.md) for the provider-specific parameters and requirements.

