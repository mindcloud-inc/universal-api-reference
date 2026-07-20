# Seven: Get HLR Lookup

Retrieves HLR lookup details from Seven.

```
GET https://connect.mindcloud.co/v1/universal/seven/latest/actions/get-hlr-lookup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seven `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seven/latest/actions/get-hlr-lookup?connectionId=$CONNECTION_ID&number=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "number": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seven/latest/actions/get-hlr-lookup?${params}`, {
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
| `number` | string | yes | The number to be queried. Multiple numbers must be separated by commas. You can enter almost any format; the API formats the number automatically. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country_code": "string",
      "country_name": "Ava Chen",
      "country_prefix": "string",
      "current_carrier": {
        "country": "string",
        "name": "Ava Chen",
        "network_code": "string",
        "network_type": "string"
      },
      "gsm_code": "string",
      "gsm_message": "string",
      "international_format_number": "string",
      "international_formatted": "string",
      "lookup_outcome": true,
      "lookup_outcome_message": "string",
      "national_format_number": "string",
      "original_carrier": {
        "country": "string",
        "name": "Ava Chen",
        "network_code": "string",
        "network_type": "string"
      },
      "ported": "string",
      "reachable": "string",
      "roaming": "string",
      "status": true,
      "status_message": "string",
      "valid_number": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country_code` | string |  |
| `country_name` | string |  |
| `country_prefix` | string |  |
| `current_carrier` | object |  |
| `current_carrier.country` | string |  |
| `current_carrier.name` | string |  |
| `current_carrier.network_code` | string |  |
| `current_carrier.network_type` | string |  |
| `gsm_code` | string |  |
| `gsm_message` | string |  |
| `international_format_number` | string |  |
| `international_formatted` | string |  |
| `lookup_outcome` | boolean |  |
| `lookup_outcome_message` | string |  |
| `national_format_number` | string |  |
| `original_carrier` | object |  |
| `original_carrier.country` | string |  |
| `original_carrier.name` | string |  |
| `original_carrier.network_code` | string |  |
| `original_carrier.network_type` | string |  |
| `ported` | string |  |
| `reachable` | string |  |
| `roaming` | string |  |
| `status` | boolean |  |
| `status_message` | string |  |
| `valid_number` | string |  |

## Native endpoint

Through the native Seven API, this operation is `GET /lookup/hlr` (base URL `https://gateway.seven.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-hlr-lookup.md) for the provider-specific parameters and requirements.

