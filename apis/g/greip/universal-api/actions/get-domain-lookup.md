# Greip - Fraud Prevention: Get Domain Lookup

Retrieves domain lookup data from Greip.

```
GET https://connect.mindcloud.co/v1/universal/greip/latest/actions/get-domain-lookup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Greip - Fraud Prevention `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/greip/latest/actions/get-domain-lookup?connectionId=$CONNECTION_ID&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/greip/latest/actions/get-domain-lookup?${params}`, {
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
| `domain` | string | yes | The fully qualified domain name to look up. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "is_bimi": true,
      "is_dangerous": true,
      "is_dkim": true,
      "is_dmarc": true,
      "is_mx": true,
      "is_new": true,
      "is_spf": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `is_bimi` | boolean |  |
| `is_dangerous` | boolean |  |
| `is_dkim` | boolean |  |
| `is_dmarc` | boolean |  |
| `is_mx` | boolean |  |
| `is_new` | boolean |  |
| `is_spf` | boolean |  |
| `name` | string |  |

## Native endpoint

Through the native Greip - Fraud Prevention API, this operation is `GET /lookup/domain` (base URL `https://greipapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-domain-lookup.md) for the provider-specific parameters and requirements.

