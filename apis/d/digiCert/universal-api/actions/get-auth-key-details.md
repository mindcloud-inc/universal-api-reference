# DigiCert: Get Auth Key Details

Retrieves details for an AuthKey in DigiCert.

```
GET https://connect.mindcloud.co/v1/universal/digiCert/latest/actions/get-auth-key-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DigiCert `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/digiCert/latest/actions/get-auth-key-details?connectionId=$CONNECTION_ID&authKeyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "authKeyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/digiCert/latest/actions/get-auth-key-details?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `authKeyId` | string | yes | The DigiCert AuthKey identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `name` | string |  |
| `status` | string |  |

## Native endpoint

Through the native DigiCert API, this operation is `GET /account/auth-key/:auth_key_id` (base URL `https://www.digicert.com/services/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-auth-key-details.md) for the provider-specific parameters and requirements.

