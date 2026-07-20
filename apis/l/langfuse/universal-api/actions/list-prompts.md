# Langfuse: List Prompts

Retrieves prompts from Langfuse.

```
GET https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/list-prompts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Langfuse `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/list-prompts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/list-prompts?${params}`, {
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
| `fromUpdatedAt` | string | no |  |
| `label` | string | no |  |
| `name` | string | no |  |
| `tag` | string | no |  |
| `toUpdatedAt` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "labels": [
        "string"
      ],
      "lastConfig": "string",
      "lastUpdatedAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "tags": [
        "string"
      ],
      "type": "string",
      "versions": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `labels` | array<string> |  |
| `lastConfig` | string |  |
| `lastUpdatedAt` | date |  |
| `name` | string |  |
| `tags` | array<string> |  |
| `type` | string |  |
| `versions` | array<number> |  |

## Native endpoint

Through the native Langfuse API, this operation is `GET /v2/prompts` (base URL `https://cloud.langfuse.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-prompts.md) for the provider-specific parameters and requirements.

