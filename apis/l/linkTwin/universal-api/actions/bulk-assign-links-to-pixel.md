# LinkTwin: Bulk Assign Links To Pixel

Adds or removes multiple links for a pixel in LinkTwin.

```
PUT https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/bulk-assign-links-to-pixel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkTwin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/bulk-assign-links-to-pixel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "493"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/bulk-assign-links-to-pixel', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "493"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Example: `493`. |
| `add` | object | no | Example: `101,102,103`. |
| `remove` | object | no | Example: `50,51`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "added": [
        1
      ],
      "error": 1,
      "errors": [
        1
      ],
      "pixel_id": 1,
      "removed": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `added` | array<number> |  |
| `error` | number |  |
| `errors` | array<number> |  |
| `pixel_id` | number |  |
| `removed` | array<number> |  |

## Native endpoint

Through the native LinkTwin API, this operation is `POST /pixel/:id/links` (base URL `https://linktw.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-assign-links-to-pixel.md) for the provider-specific parameters and requirements.

