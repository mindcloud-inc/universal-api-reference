# Ice and Fire (Game of Thrones): Get Character



```
GET https://connect.mindcloud.co/v1/universal/iceAndFireGameOfThrones/latest/actions/get-character
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ice and Fire (Game of Thrones) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iceAndFireGameOfThrones/latest/actions/get-character?connectionId=$CONNECTION_ID&characterId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "characterId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iceAndFireGameOfThrones/latest/actions/get-character?${params}`, {
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
| `characterId` | number | yes | The numeric ID of the character to retrieve. |

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

Through the native Ice and Fire (Game of Thrones) API, this operation is `GET /characters/:characterId` (base URL `https://anapioficeandfire.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-character.md) for the provider-specific parameters and requirements.

