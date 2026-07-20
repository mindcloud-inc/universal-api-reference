# SureContact: List Tags

Retrieves available contact tags from SureContact.

```
GET https://connect.mindcloud.co/v1/universal/sureContact/latest/actions/list-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SureContact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sureContact/latest/actions/list-tags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sureContact/latest/actions/list-tags?${params}`, {
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
| `archived` | string | no | Filter tags by archive status. |
| `direction` | string | no | Sort direction: asc or desc. |
| `perPage` | number | no | Number of items per page. |
| `search` | string | no | Search tags by name or slug. |
| `sort` | string | no | Sort field. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "name": "Ava Chen",
      "slug": "string",
      "usage_count": 1,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `created_at` | date |  |
| `description` | string |  |
| `name` | string |  |
| `slug` | string |  |
| `usage_count` | number |  |
| `uuid` | string |  |

## Native endpoint

Through the native SureContact API, this operation is `GET api/v1/public/tags` (base URL `https://api.surecontact.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tags.md) for the provider-specific parameters and requirements.

