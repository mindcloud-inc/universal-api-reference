# Nozbe Personal: Create Tag

Creates a new tag in Nozbe Personal.

```
POST https://connect.mindcloud.co/v1/universal/nozbePersonal/latest/actions/create-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nozbe Personal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nozbePersonal/latest/actions/create-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Codex Tag"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nozbePersonal/latest/actions/create-tag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Codex Tag"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Tag name. Example: `Codex Tag`. |
| `teamId` | string | no | Optional team that owns the tag. Example: `L2TZ05o6wV41fjMe`. |
| `color` | string | no | Optional tag color. Example: `green`. |
| `icon` | string | no | Optional tag icon. Example: `folder`. |
| `isFavorite` | boolean | no | Whether the tag is a favorite. Default: `false`. Example: `false`. |

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

Through the native Nozbe Personal API, this operation is `POST /tags` (base URL `https://api4.nozbe.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tag.md) for the provider-specific parameters and requirements.

