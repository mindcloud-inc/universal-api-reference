# Seven: Get MNP Lookup

Retrieves MNP lookup details from Seven.

```
GET https://connect.mindcloud.co/v1/universal/seven/latest/actions/get-mnp-lookup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seven `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seven/latest/actions/get-mnp-lookup?connectionId=$CONNECTION_ID&number=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "number": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seven/latest/actions/get-mnp-lookup?${params}`, {
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
      "code": 1,
      "mnp": {
        "country": "string",
        "international_formatted": "string",
        "isPorted": true,
        "mccmnc": "string",
        "national_format": "string",
        "network": "string",
        "network_type": "string",
        "number": "string"
      },
      "price": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `mnp` | object |  |
| `mnp.country` | string |  |
| `mnp.international_formatted` | string |  |
| `mnp.isPorted` | boolean |  |
| `mnp.mccmnc` | string |  |
| `mnp.national_format` | string |  |
| `mnp.network` | string |  |
| `mnp.network_type` | string |  |
| `mnp.number` | string |  |
| `price` | number |  |
| `success` | boolean |  |

## Native endpoint

Through the native Seven API, this operation is `GET /lookup/mnp` (base URL `https://gateway.seven.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-mnp-lookup.md) for the provider-specific parameters and requirements.

