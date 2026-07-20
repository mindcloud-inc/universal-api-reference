# BuildBetter: Get Person By ID



```
GET https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/get-person-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BuildBetter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/get-person-by-id?connectionId=$CONNECTION_ID&id=12345" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "12345"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/buildBetter/latest/actions/get-person-by-id?${params}`, {
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
| `id` | string | yes | BuildBetter person ID. Example: `12345`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": {},
      "company_id": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": "string",
      "last_name": "Chen",
      "source": "string",
      "source_identifier": "string",
      "title": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | object | Linked company summary. |
| `company_id` | string | Linked company identifier. |
| `email` | string | Person email address. |
| `first_name` | string | Person first name. |
| `id` | string | BuildBetter person identifier. |
| `last_name` | string | Person last name. |
| `source` | string | BuildBetter source classification. |
| `source_identifier` | string | Provider source identifier. |
| `title` | string | Person job title. |
| `updated_at` | date | Last updated timestamp. |

## Native endpoint

Through the native BuildBetter API, this operation is `POST /graphql` (base URL `https://api.buildbetter.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-person-by-id.md) for the provider-specific parameters and requirements.

