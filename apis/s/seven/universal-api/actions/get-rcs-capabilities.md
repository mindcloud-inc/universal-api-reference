# Seven: Get RCS Capabilities

Retrieves RCS capabilities from Seven.

```
GET https://connect.mindcloud.co/v1/universal/seven/latest/actions/get-rcs-capabilities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seven `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seven/latest/actions/get-rcs-capabilities?connectionId=$CONNECTION_ID&number=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "number": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/seven/latest/actions/get-rcs-capabilities?${params}`, {
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
| `from` | string | no | To check the RCS capabilities of a phone number, the respective agent identifier is always required. By default, our API uses the first RCS sender ID in your account. You can use a different agent with this parameter. |

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
      "rcs_capabilities": [
        "string"
      ],
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
| `rcs_capabilities` | array<string> |  |
| `success` | boolean |  |

## Native endpoint

Through the native Seven API, this operation is `GET /lookup/rcs` (base URL `https://gateway.seven.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-rcs-capabilities.md) for the provider-specific parameters and requirements.

