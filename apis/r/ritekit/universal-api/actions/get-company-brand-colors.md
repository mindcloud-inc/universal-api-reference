# Ritekit: Get Company Brand Colors

Retrieves company brand colors from Ritekit.

```
GET https://connect.mindcloud.co/v1/universal/ritekit/latest/actions/get-company-brand-colors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ritekit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ritekit/latest/actions/get-company-brand-colors?connectionId=$CONNECTION_ID&companyNameOrDomain=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyNameOrDomain": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ritekit/latest/actions/get-company-brand-colors?${params}`, {
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
| `companyNameOrDomain` | string | yes | Company name or domain to inspect for brand colors. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        "string"
      ],
      "message": "string",
      "name": "Ava Chen",
      "result": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<string> |  |
| `message` | string |  |
| `name` | string |  |
| `result` | boolean |  |

## Native endpoint

Through the native Ritekit API, this operation is `GET /v2/company-insights/brand-colors` (base URL `https://api.ritekit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-brand-colors.md) for the provider-specific parameters and requirements.

