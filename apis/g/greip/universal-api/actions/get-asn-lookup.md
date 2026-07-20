# Greip - Fraud Prevention: Get ASN Lookup

Retrieves ASN lookup data from Greip.

```
GET https://connect.mindcloud.co/v1/universal/greip/latest/actions/get-asn-lookup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Greip - Fraud Prevention `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/greip/latest/actions/get-asn-lookup?connectionId=$CONNECTION_ID&asn=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "asn": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/greip/latest/actions/get-asn-lookup?${params}`, {
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
| `asn` | string | yes | The autonomous system number to look up, such as AS6167 or 6167. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "asn": "string",
      "country": "string",
      "created": "string",
      "domain": "string",
      "email": "ava@example.com",
      "name": "Ava Chen",
      "org": "string",
      "phone": "string",
      "prefixes": {},
      "registry": "string",
      "status": "string",
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
| `country` | string |  |
| `created` | string |  |
| `domain` | string |  |
| `email` | string |  |
| `name` | string |  |
| `org` | string |  |
| `phone` | string |  |
| `prefixes` | object |  |
| `registry` | string |  |
| `status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Greip - Fraud Prevention API, this operation is `GET /lookup/asn` (base URL `https://greipapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-asn-lookup.md) for the provider-specific parameters and requirements.

