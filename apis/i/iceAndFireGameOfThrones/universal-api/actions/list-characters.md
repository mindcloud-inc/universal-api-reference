# Ice and Fire (Game of Thrones): List Characters



```
GET https://connect.mindcloud.co/v1/universal/iceAndFireGameOfThrones/latest/actions/list-characters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ice and Fire (Game of Thrones) `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iceAndFireGameOfThrones/latest/actions/list-characters?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iceAndFireGameOfThrones/latest/actions/list-characters?${params}`, {
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
| `name` | string | no | Return only characters with this exact name. |
| `gender` | string | no | Return only characters with this gender. |
| `culture` | string | no | Return only characters from this culture. |
| `born` | string | no | Return only characters born in this year string. |
| `died` | string | no | Return only characters who died in this year string. |
| `isAlive` | boolean | no | Return only characters who are alive or dead. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aliases": [
        "string"
      ],
      "allegiances": [
        "string"
      ],
      "books": [
        "string"
      ],
      "born": "string",
      "culture": "string",
      "died": "string",
      "father": "string",
      "gender": "string",
      "mother": "string",
      "name": "Ava Chen",
      "playedBy": [
        "string"
      ],
      "povBooks": [
        "string"
      ],
      "spouse": "string",
      "titles": [
        "string"
      ],
      "tvSeries": [
        "string"
      ],
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aliases` | array<string> |  |
| `allegiances` | array<string> |  |
| `books` | array<string> |  |
| `born` | string |  |
| `culture` | string |  |
| `died` | string |  |
| `father` | string |  |
| `gender` | string |  |
| `mother` | string |  |
| `name` | string |  |
| `playedBy` | array<string> |  |
| `povBooks` | array<string> |  |
| `spouse` | string |  |
| `titles` | array<string> |  |
| `tvSeries` | array<string> |  |
| `url` | string |  |

## Native endpoint

Through the native Ice and Fire (Game of Thrones) API, this operation is `GET /characters` (base URL `https://anapioficeandfire.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-characters.md) for the provider-specific parameters and requirements.

