# Timewax: Update Position

Updates an existing position in Timewax.

```
PUT https://connect.mindcloud.co/v1/universal/timewax/latest/actions/update-position
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timewax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/timewax/latest/actions/update-position" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "request.position": "string",
  "request.item.code": "string",
  "request.item.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timewax/latest/actions/update-position', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "request.position": "string",
    "request.item.code": "string",
    "request.item.name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `request.position` | string | yes | Required. Code or name of the position to edit. |
| `request.item.code` | string | yes | Required. New code of the position. |
| `request.item.name` | string | yes | Required. New name of the position. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "valid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `valid` | string | Operation validity indicator. |

## Native endpoint

Through the native Timewax API, this operation is `POST position/edit/` (base URL `https://api.timewax.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-position.md) for the provider-specific parameters and requirements.

