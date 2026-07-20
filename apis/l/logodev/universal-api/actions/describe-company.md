# Logo.dev: Describe Company

Retrieves company details from Logo.dev by domain.

```
GET https://connect.mindcloud.co/v1/universal/logodev/latest/actions/describe-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Logo.dev `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logodev/latest/actions/describe-company?connectionId=$CONNECTION_ID&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/logodev/latest/actions/describe-company?${params}`, {
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
| `domain` | string | yes | Company domain to describe. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blurhash": "string",
      "colors": [
        {}
      ],
      "description": "string",
      "domain": "string",
      "indexed_at": "2026-05-07T12:00:00.000Z",
      "logo": "string",
      "name": "Ava Chen",
      "socials": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blurhash` | string |  |
| `colors` | array<object> |  |
| `description` | string |  |
| `domain` | string |  |
| `indexed_at` | date |  |
| `logo` | string |  |
| `name` | string |  |
| `socials` | object |  |

## Native endpoint

Through the native Logo.dev API, this operation is `GET /describe/:domain` (base URL `https://api.logo.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/describe-company.md) for the provider-specific parameters and requirements.

