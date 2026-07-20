# Shadify: Generate Takuzu Puzzle

Retrieves a random Takuzu puzzle from Shadify.

```
GET https://connect.mindcloud.co/v1/universal/shadify/latest/actions/generate-takuzu-puzzle
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shadify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shadify/latest/actions/generate-takuzu-puzzle?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shadify/latest/actions/generate-takuzu-puzzle?${params}`, {
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
| `size` | number | no | Optional even field size from 4 to 12. Default is 8. Default: `8`. |
| `fill` | number | no | Optional fill level from 0 to 100 percent. Default is 33. Default: `33`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "field": [
        [
          "string"
        ]
      ],
      "size": 1,
      "task": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `field` | array<array> | Solved Takuzu field. |
| `size` | number | Generated field size. |
| `task` | array<array> | Takuzu task with x placeholders. |

## Native endpoint

Through the native Shadify API, this operation is `GET /takuzu/generator` (base URL `https://shadify.yurace.pro/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-takuzu-puzzle.md) for the provider-specific parameters and requirements.

