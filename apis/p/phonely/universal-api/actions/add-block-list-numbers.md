# Phonely: Add Block List Numbers

Adds phone numbers to the Phonely block list.

```
POST https://connect.mindcloud.co/v1/universal/phonely/latest/actions/add-block-list-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Phonely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/phonely/latest/actions/add-block-list-numbers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uid": "string",
  "agentId": "string",
  "numbers[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/phonely/latest/actions/add-block-list-numbers', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uid": "string",
    "agentId": "string",
    "numbers[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `uid` | string | yes |  |
| `agentId` | string | yes |  |
| `numbers[]` | array<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "added": [
        "string"
      ],
      "failed": [
        "string"
      ],
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `added` | array<string> |  |
| `failed` | array<string> |  |
| `message` | string |  |

## Native endpoint

Through the native Phonely API, this operation is `POST /api/agent-block-list` (base URL `https://app.phonely.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-block-list-numbers.md) for the provider-specific parameters and requirements.

