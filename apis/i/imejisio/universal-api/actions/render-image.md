# Imejis.io: Render Image

Creates a rendered image in Imejis.io by design ID.

```
POST https://connect.mindcloud.co/v1/universal/imejisio/latest/actions/render-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Imejis.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/imejisio/latest/actions/render-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "designId": "HxQGYmW6hKu-HAORyRazt"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/imejisio/latest/actions/render-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "designId": "HxQGYmW6hKu-HAORyRazt"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `designId` | string | yes | The Imejis.io template design identifier to render. Example: `HxQGYmW6hKu-HAORyRazt`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<number> | Byte array for the rendered image binary returned by the current raw-response runtime surface. |
| `type` | string | Buffer marker for the rendered image payload returned by the current raw-response runtime surface. |

## Native endpoint

Through the native Imejis.io API, this operation is `POST :design_id` (base URL `https://render.imejis.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/render-image.md) for the provider-specific parameters and requirements.

