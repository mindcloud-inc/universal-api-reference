# Salesflare: List Pipelines



```
GET https://connect.mindcloud.co/v1/universal/salesflare/latest/actions/list-pipelines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesflare `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesflare/latest/actions/list-pipelines?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesflare/latest/actions/list-pipelines?${params}`, {
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
| `orderBy` | string | no | Sort expression for pipelines. |
| `search` | string | no | Free-text search across pipelines. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "defaultPipeline": true,
      "id": 1,
      "name": "Ava Chen",
      "order": 1,
      "stages": [
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
| `defaultPipeline` | boolean |  |
| `id` | number |  |
| `name` | string |  |
| `order` | number |  |
| `stages` | array<object> |  |

## Native endpoint

Through the native Salesflare API, this operation is `GET pipelines` (base URL `https://api.salesflare.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pipelines.md) for the provider-specific parameters and requirements.

