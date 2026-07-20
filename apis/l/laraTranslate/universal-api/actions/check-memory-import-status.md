# Lara Translate: Check memory import status

Retrieves the status of a Lara Translate memory import.

```
GET https://connect.mindcloud.co/v1/universal/laraTranslate/latest/actions/check-memory-import-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lara Translate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/laraTranslate/latest/actions/check-memory-import-status?connectionId=$CONNECTION_ID&id=imp_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "imp_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/laraTranslate/latest/actions/check-memory-import-status?${params}`, {
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
| `id` | string | yes | ID of the memory import job to inspect. Example: `imp_123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "begin": 1,
      "channel": 1,
      "end": 1,
      "id": "string",
      "progress": 1,
      "size": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `begin` | number |  |
| `channel` | number |  |
| `end` | number |  |
| `id` | string |  |
| `progress` | number |  |
| `size` | number |  |

## Native endpoint

Through the native Lara Translate API, this operation is `POST /` (base URL `https://mcp-v2.laratranslate.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-memory-import-status.md) for the provider-specific parameters and requirements.

