# Gemini: List Batches

Retrieves a list of batches from Gemini.

```
GET https://connect.mindcloud.co/v1/universal/gemini/latest/actions/list-batches
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gemini `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gemini/latest/actions/list-batches?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gemini/latest/actions/list-batches?${params}`, {
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
| `filter` | string | no | Optional filter expression for batch listing. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `returnPartialSuccess` | boolean | no | Whether to return partial success results. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "done": true,
      "error": {
        "message": "string"
      },
      "metadata": {
        "createTime": "2026-05-07T12:00:00.000Z",
        "displayName": "Ava Chen",
        "endTime": "2026-05-07T12:00:00.000Z",
        "model": "string",
        "state": "string",
        "updateTime": "2026-05-07T12:00:00.000Z"
      },
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `done` | boolean | Whether the long-running batch operation is complete. |
| `error.message` | string | Batch-level error message when present. |
| `metadata.createTime` | date | Batch creation timestamp. |
| `metadata.displayName` | string | Display name configured for the batch. |
| `metadata.endTime` | date | Batch completion timestamp, when available. |
| `metadata.model` | string | Model used by the batch. |
| `metadata.state` | string | Current batch state. |
| `metadata.updateTime` | date | Last batch update timestamp. |
| `name` | string | Batch operation resource name. |

## Native endpoint

Through the native Gemini API, this operation is `GET v1beta/:name` (base URL `https://generativelanguage.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-batches.md) for the provider-specific parameters and requirements.

