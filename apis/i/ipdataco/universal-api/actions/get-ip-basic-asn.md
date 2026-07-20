# ipdata.co: Get IP Basic ASN



```
GET https://connect.mindcloud.co/v1/universal/ipdataco/latest/actions/get-ip-basic-asn
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ipdata.co `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ipdataco/latest/actions/get-ip-basic-asn?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ipdataco/latest/actions/get-ip-basic-asn?${params}`, {
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
| `ip` | string | no | The IP address to look up. Default: `8.8.8.8`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "asn": "string",
      "domain": "string",
      "name": "Ava Chen",
      "route": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `asn` | string |  |
| `domain` | string |  |
| `name` | string |  |
| `route` | string |  |
| `type` | string |  |

## Native endpoint

Through the native ipdata.co API, this operation is `GET /:ip/asn` (base URL `https://api.ipdata.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ip-basic-asn.md) for the provider-specific parameters and requirements.

