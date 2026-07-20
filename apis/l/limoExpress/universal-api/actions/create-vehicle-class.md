# LimoExpress: Create Vehicle Class

Creates a new vehicle class in LimoExpress.

```
POST https://connect.mindcloud.co/v1/universal/limoExpress/latest/actions/create-vehicle-class
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LimoExpress `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/limoExpress/latest/actions/create-vehicle-class" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "active": true,
  "availableForPublic": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/limoExpress/latest/actions/create-vehicle-class', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "active": true,
    "availableForPublic": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the vehicle class |
| `active` | boolean | yes | Active flag for vehicle class |
| `availableForPublic` | boolean | yes | Whether class is available on public booking page |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
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
| `data` | object | Operation payload when returned by the API. |
| `message` | string | Operation status or error message. |
| `success` | boolean | Operation success flag when provided by the API. |

## Native endpoint

Through the native LimoExpress API, this operation is `PUT /api/integration/vehicle-classes` (base URL `https://api.limoexpress.me`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-vehicle-class.md) for the provider-specific parameters and requirements.

