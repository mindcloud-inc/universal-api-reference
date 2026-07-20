# BunnyCDN: Add Custom Certificate

Adds a custom certificate to a BunnyCDN pull zone.

```
POST https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/add-custom-certificate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BunnyCDN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/add-custom-certificate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "hostname": "Ava Chen",
  "certificate": "string",
  "certificateKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/add-custom-certificate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "hostname": "Ava Chen",
    "certificate": "string",
    "certificateKey": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The Bunny pull zone ID. |
| `hostname` | string | yes | Hostname to attach the custom certificate to. |
| `certificate` | string | yes | Base64-encoded certificate content. |
| `certificateKey` | string | yes | Base64-encoded private key content. |

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
| `ErrorKey` | string | Machine-readable Bunny error key returned when the request fails. |
| `Field` | string | Entity field associated with the Bunny error. |
| `Message` | string | Human-readable Bunny error message. |

## Native endpoint

Through the native BunnyCDN API, this operation is `POST /pullzone/:id/addCertificate` (base URL `https://api.bunny.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-custom-certificate.md) for the provider-specific parameters and requirements.

