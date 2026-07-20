# Brasil API: Get Domain Status

Retrieves a .br domain status from Brasil API.

```
GET https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/get-domain-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brasil API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/get-domain-status?connectionId=$CONNECTION_ID&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brasilAPI/latest/actions/get-domain-status?${params}`, {
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
| `domain` | string | yes | The .br domain to evaluate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expires-at": "string",
      "fqdn": "string",
      "hosts": [
        "string"
      ],
      "publication-status": "string",
      "reasons": [
        "string"
      ],
      "status": "string",
      "status_code": 1,
      "suggestions": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expires-at` | string |  |
| `fqdn` | string |  |
| `hosts` | array<string> |  |
| `publication-status` | string |  |
| `reasons` | array<string> |  |
| `status` | string |  |
| `status_code` | number |  |
| `suggestions` | array<string> |  |

## Native endpoint

Through the native Brasil API API, this operation is `GET /registrobr/v1/{domain}` (base URL `https://brasilapi.com.br/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-domain-status.md) for the provider-specific parameters and requirements.

