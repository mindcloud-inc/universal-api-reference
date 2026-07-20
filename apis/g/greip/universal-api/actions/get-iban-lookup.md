# Greip - Fraud Prevention: Get IBAN Lookup

Retrieves IBAN lookup data from Greip.

```
GET https://connect.mindcloud.co/v1/universal/greip/latest/actions/get-iban-lookup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Greip - Fraud Prevention `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/greip/latest/actions/get-iban-lookup?connectionId=$CONNECTION_ID&iban=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "iban": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/greip/latest/actions/get-iban-lookup?${params}`, {
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
| `iban` | string | yes | The IBAN value to validate and enrich. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country": {},
      "custom_rules_applied": {},
      "formats": {},
      "isValid": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | object |  |
| `custom_rules_applied` | object |  |
| `formats` | object |  |
| `isValid` | boolean |  |

## Native endpoint

Through the native Greip - Fraud Prevention API, this operation is `GET /lookup/iban` (base URL `https://greipapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-iban-lookup.md) for the provider-specific parameters and requirements.

