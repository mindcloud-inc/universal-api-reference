# Eledo: List Templates

Retrieves a list of templates from Eledo.

```
GET https://connect.mindcloud.co/v1/universal/eledo/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eledo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eledo/latest/actions/list-templates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eledo/latest/actions/list-templates?${params}`, {
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
| `scope` | string | no | Use Mine or Public to choose template scope. |
| `limit` | number | no |  |
| `page` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bulk": true,
      "date": 1,
      "id": "string",
      "name": "Ava Chen",
      "thumbnailUrl": "https://example.com",
      "type": 1,
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bulk` | boolean |  |
| `date` | number |  |
| `id` | string |  |
| `name` | string |  |
| `thumbnailUrl` | string |  |
| `type` | number |  |
| `version` | number |  |

## Native endpoint

Through the native Eledo API, this operation is `GET /List` (base URL `https://eledo.online/api/RESTv1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

