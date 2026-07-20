# Shadify: Start Set Game

Retrieves a new Set game state from Shadify.

```
GET https://connect.mindcloud.co/v1/universal/shadify/latest/actions/start-set-game
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shadify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shadify/latest/actions/start-set-game?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shadify/latest/actions/start-set-game?${params}`, {
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
| `possibleSets` | boolean | no | Optional true or false value that includes possible set hints. Default is true. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "freeCards": [
        {}
      ],
      "layout": [
        {}
      ],
      "possibleSets": [
        [
          "string"
        ]
      ],
      "state": "string",
      "wonCards": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `freeCards` | array<object> | Cards not currently in play. |
| `layout` | array<object> | Cards available on the table. |
| `possibleSets` | array<array> | Possible set combinations. |
| `state` | string | Serializable game state. |
| `wonCards` | array<object> | Cards already won. |

## Native endpoint

Through the native Shadify API, this operation is `GET /set/start` (base URL `https://shadify.yurace.pro/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-set-game.md) for the provider-specific parameters and requirements.

