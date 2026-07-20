# Phonely: Delete Block List Numbers

Deletes phone numbers from the Phonely block list.

```
DELETE https://connect.mindcloud.co/v1/universal/phonely/latest/actions/delete-block-list-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Phonely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/phonely/latest/actions/delete-block-list-numbers?connectionId=$CONNECTION_ID&uid=string&agentId=string&numbers%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uid": "string",
  "agentId": "string",
  "numbers[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/phonely/latest/actions/delete-block-list-numbers?${params}`, {
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
| `uid` | string | yes |  |
| `agentId` | string | yes |  |
| `numbers[]` | array<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "failed": [
        "string"
      ],
      "message": "string",
      "removed": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `failed` | array<string> |  |
| `message` | string |  |
| `removed` | array<string> |  |

## Native endpoint

Through the native Phonely API, this operation is `DELETE /api/agent-block-list` (base URL `https://app.phonely.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-block-list-numbers.md) for the provider-specific parameters and requirements.

