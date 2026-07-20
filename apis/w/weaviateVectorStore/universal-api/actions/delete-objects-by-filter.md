# Weaviate Vector Store: Delete Objects By Filter

Deletes objects in batch from Weaviate.

```
DELETE https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/delete-objects-by-filter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weaviate Vector Store `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/delete-objects-by-filter?connectionId=$CONNECTION_ID&match.class=string&match.where.path%5B0%5D=title&match.where.operator=Equal&match.where.valueText=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "match.class": "string",
  "match.where.path[0]": "title",
  "match.where.operator": "Equal",
  "match.where.valueText": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weaviateVectorStore/latest/actions/delete-objects-by-filter?${params}`, {
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
| `match.class` | string | yes |  |
| `match.where.path[0]` | string | yes | Default: `title`. |
| `match.where.operator` | string | yes | Default: `Equal`. |
| `match.where.valueText` | string | yes |  |
| `output` | string | no | Default: `verbose`. |
| `dryRun` | boolean | no | Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deletionTimeUnixMilli": 1,
      "dryRun": true,
      "match": {
        "class": "string",
        "where": {
          "operator": "string",
          "path": [
            [
              "string"
            ]
          ],
          "valueText": "string"
        }
      },
      "output": "string",
      "results": {
        "failed": 1,
        "limit": 1,
        "matches": 1,
        "objects": [
          {
            "id": "string",
            "status": "string"
          }
        ],
        "successful": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deletionTimeUnixMilli` | number |  |
| `dryRun` | boolean |  |
| `match.class` | string |  |
| `match.where.operator` | string |  |
| `match.where.path[]` | array<string> |  |
| `match.where.valueText` | string |  |
| `output` | string |  |
| `results.failed` | number |  |
| `results.limit` | number |  |
| `results.matches` | number |  |
| `results.objects[].id` | string |  |
| `results.objects[].status` | string |  |
| `results.successful` | number |  |

## Native endpoint

Through the native Weaviate Vector Store API, this operation is `DELETE /v1/batch/objects` (base URL `https://tl3apaxxsoiuwhpnsdv19a.c0.us-west3.gcp.weaviate.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-objects-by-filter.md) for the provider-specific parameters and requirements.

