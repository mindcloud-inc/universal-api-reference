# Scanova: Restore QR Code From Trash



```
PUT https://connect.mindcloud.co/v1/universal/scanova/latest/actions/restore-qr-code-from-trash
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scanova `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/scanova/latest/actions/restore-qr-code-from-trash" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "qrid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scanova/latest/actions/restore-qr-code-from-trash', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "qrid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `qrid` | string | yes | QR Code ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native Scanova API, this operation is `POST /qrcode/trash/{qrid}/restore/` (base URL `https://management.scanova.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/restore-qr-code-from-trash.md) for the provider-specific parameters and requirements.

