# Phrase: Get Account

Retrieves a single account from Phrase.

```
GET https://connect.mindcloud.co/v1/universal/phrase/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Phrase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/phrase/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/phrase/latest/actions/get-account?${params}`, {
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
| `id` | string | no | Phrase account id to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": "string",
      "company_logo_url": "https://example.com",
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "roles": [
        "string"
      ],
      "slug": "string",
      "subscription": {},
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | string |  |
| `company_logo_url` | string |  |
| `created_at` | date |  |
| `id` | string |  |
| `name` | string |  |
| `roles` | array<string> |  |
| `slug` | string |  |
| `subscription` | object |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Phrase API, this operation is `GET /accounts/{id}` (base URL `https://api.phrase.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

