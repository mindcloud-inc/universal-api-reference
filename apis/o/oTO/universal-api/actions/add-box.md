# OTO: Add Box

Creates a new box in OTO.

```
POST https://connect.mindcloud.co/v1/universal/oTO/latest/actions/add-box
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OTO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oTO/latest/actions/add-box" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "length": 1,
  "width": 1,
  "height": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oTO/latest/actions/add-box', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "length": 1,
    "width": 1,
    "height": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name for the new box template. |
| `length` | number | yes | Box length. |
| `width` | number | yes | Box width. |
| `height` | number | yes | Box height. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native OTO API, this operation is `POST /addBox` (base URL `https://api.tryoto.com/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-box.md) for the provider-specific parameters and requirements.

