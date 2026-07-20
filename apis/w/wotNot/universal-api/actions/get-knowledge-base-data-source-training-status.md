# WotNot: Get Knowledge Base Data Source Training Status

Retrieves knowledge base source training status from WotNot.

```
GET https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/get-knowledge-base-data-source-training-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WotNot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/get-knowledge-base-data-source-training-status?connectionId=$CONNECTION_ID&sourceIds=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sourceIds": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/get-knowledge-base-data-source-training-status?${params}`, {
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
| `sourceIds` | string | yes | Comma-separated knowledge base source IDs |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ok": true,
      "sources": [
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
| `ok` | boolean |  |
| `sources` | array<object> |  |

## Native endpoint

Through the native WotNot API, this operation is `GET /api/v1/ai/status/sources` (base URL `https://api.wotnot.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-knowledge-base-data-source-training-status.md) for the provider-specific parameters and requirements.

