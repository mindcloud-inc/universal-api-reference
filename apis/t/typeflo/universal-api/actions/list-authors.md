# Typeflo: List Authors

Retrieves author profiles from the Typeflo site.

```
GET https://connect.mindcloud.co/v1/universal/typeflo/latest/actions/list-authors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Typeflo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typeflo/latest/actions/list-authors?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/typeflo/latest/actions/list-authors?${params}`, {
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
| `slug` | string | no | Filter authors by their unique slug. |
| `name` | string | no | Filter authors by name. |
| `email` | string | no | Filter authors by email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatar": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "email": "ava@example.com",
      "id": "string",
      "metadescription": "string",
      "name": "Ava Chen",
      "slug": "string",
      "socials": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar` | string | Avatar URL for the author. |
| `createdAt` | date | When the author record was created. |
| `description` | string | Author bio or description. |
| `email` | string | The author email address. |
| `id` | string | The unique ID of the author. |
| `metadescription` | string | Meta description for the author. |
| `name` | string | The display name of the author. |
| `slug` | string | The unique slug of the author. |
| `socials` | object | Social profile metadata for the author when configured. |

## Native endpoint

Through the native Typeflo API, this operation is `GET /content/authors` (base URL `https://{{credentials.subdomain}}.typeflo.io/api/headless`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-authors.md) for the provider-specific parameters and requirements.

