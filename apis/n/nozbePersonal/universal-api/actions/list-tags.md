# Nozbe Personal: List Tags

Retrieves accessible tags from Nozbe Personal.

```
GET https://connect.mindcloud.co/v1/universal/nozbePersonal/latest/actions/list-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nozbe Personal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nozbePersonal/latest/actions/list-tags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nozbePersonal/latest/actions/list-tags?${params}`, {
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
| `teamId` | string | no |  |
| `isFavorite` | boolean | no |  |
| `fields` | string | no |  |
| `sortBy` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "icon": "string",
      "id": "string",
      "isFavorite": true,
      "name": "Ava Chen",
      "teamId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `icon` | string |  |
| `id` | string |  |
| `isFavorite` | boolean |  |
| `name` | string |  |
| `teamId` | string |  |

## Native endpoint

Through the native Nozbe Personal API, this operation is `GET /tags` (base URL `https://api4.nozbe.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tags.md) for the provider-specific parameters and requirements.

