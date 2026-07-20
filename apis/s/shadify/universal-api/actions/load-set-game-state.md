# Shadify: Load Set Game State

Retrieves a Set game state from Shadify.

```
GET https://connect.mindcloud.co/v1/universal/shadify/latest/actions/load-set-game-state
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shadify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shadify/latest/actions/load-set-game-state?connectionId=$CONNECTION_ID&state=0-1-2-3-4-5-6-7-8-9-10-11" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "state": "0-1-2-3-4-5-6-7-8-9-10-11"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shadify/latest/actions/load-set-game-state?${params}`, {
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
| `state` | string | yes | Required Set game state string from a previous Start Set Game response. Default: `0-1-2-3-4-5-6-7-8-9-10-11`. |
| `possibleSets` | boolean | no | Optional true or false value that includes possible set hints. Default is true. Default: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `action` | string | no | Optional add or remove action for the current Set game state. |
| `cards` | string | no | Required for action=remove. Dash-joined card IDs such as 1-2-3. |

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

Through the native Shadify API, this operation is `GET /set/:state` (base URL `https://shadify.yurace.pro/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/load-set-game-state.md) for the provider-specific parameters and requirements.

