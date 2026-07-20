# LinkTwin: Update QR Code

Updates an existing QR code in LinkTwin.

```
PUT https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/update-qr-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LinkTwin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/update-qr-code" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "1",
  "type": "link",
  "data": "https://example.com/temp-linktwin-qr"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linkTwin/latest/actions/update-qr-code', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "1",
    "type": "link",
    "data": "https://example.com/temp-linktwin-qr"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Example: `1`. |
| `type` | string | yes | Example: `link`. |
| `data` | string | yes | Example: `https://example.com/temp-linktwin-qr`. |
| `background` | string | no | Example: `rgb(255,255,255)`. |
| `foreground` | string | no | Example: `rgb(0,0,0)`. |
| `logo` | string | no | Example: `https://example.com/logo.png`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native LinkTwin API returns.

## Native endpoint

Through the native LinkTwin API, this operation is `PUT /qr/:id/update` (base URL `https://linktw.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-qr-code.md) for the provider-specific parameters and requirements.

