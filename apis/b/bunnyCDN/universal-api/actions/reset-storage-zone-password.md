# BunnyCDN: Reset Storage Zone Password

Resets a BunnyCDN storage zone password.

```
PUT https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/reset-storage-zone-password
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BunnyCDN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/reset-storage-zone-password" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/reset-storage-zone-password', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The Bunny storage zone ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ErrorKey": "string",
      "Field": "string",
      "Message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ErrorKey` | string |  |
| `Field` | string |  |
| `Message` | string |  |

## Native endpoint

Through the native BunnyCDN API, this operation is `POST /storagezone/:id/resetPassword` (base URL `https://api.bunny.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reset-storage-zone-password.md) for the provider-specific parameters and requirements.

