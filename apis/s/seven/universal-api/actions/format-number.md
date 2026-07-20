# Seven: Format Number

Retrieves formatted phone number details from Seven.

```
GET https://connect.mindcloud.co/v1/universal/seven/latest/actions/format-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seven `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seven/latest/actions/format-number?connectionId=$CONNECTION_ID&number=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "number": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seven/latest/actions/format-number?${params}`, {
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
      "carrier": "string",
      "country_code": "string",
      "country_iso": "string",
      "country_name": "Ava Chen",
      "international": "string",
      "international_formatted": "string",
      "national": "string",
      "network_type": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `carrier` | string |  |
| `country_code` | string |  |
| `country_iso` | string |  |
| `country_name` | string |  |
| `international` | string |  |
| `international_formatted` | string |  |
| `national` | string |  |
| `network_type` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Seven API, this operation is `GET /lookup/format` (base URL `https://gateway.seven.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/format-number.md) for the provider-specific parameters and requirements.

