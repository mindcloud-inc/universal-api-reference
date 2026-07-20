# LinkTwin: Create Pixel

Creates a new tracking pixel in LinkTwin.

```
POST https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/create-pixel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkTwin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/create-pixel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "gtmpixel",
  "name": "Temp LinkTwin Pixel",
  "tag": "GTM-TEMP123"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/create-pixel', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "gtmpixel",
    "name": "Temp LinkTwin Pixel",
    "tag": "GTM-TEMP123"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | yes | Example: `gtmpixel`. |
| `name` | string | yes | Example: `Temp LinkTwin Pixel`. |
| `tag` | string | yes | Example: `GTM-TEMP123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": 1,
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | number |  |
| `id` | string |  |

## Native endpoint

Through the native LinkTwin API, this operation is `POST /pixel/add` (base URL `https://linktw.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-pixel.md) for the provider-specific parameters and requirements.

