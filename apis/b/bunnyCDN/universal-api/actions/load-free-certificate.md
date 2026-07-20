# BunnyCDN: Load Free Certificate

Loads a free certificate in BunnyCDN.

```
GET https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/load-free-certificate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BunnyCDN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/load-free-certificate?connectionId=$CONNECTION_ID&hostname=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "hostname": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bunnyCDN/latest/actions/load-free-certificate?${params}`, {
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
| `hostname` | string | yes | The hostname that the certificate should be loaded for. |

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

Through the native BunnyCDN API, this operation is `GET /pullzone/loadFreeCertificate` (base URL `https://api.bunny.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/load-free-certificate.md) for the provider-specific parameters and requirements.

