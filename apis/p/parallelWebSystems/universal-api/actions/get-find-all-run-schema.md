# Parallel Web Systems: Get FindAll Run Schema



```
GET https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/get-find-all-run-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Parallel Web Systems `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/get-find-all-run-schema?connectionId=$CONNECTION_ID&findallId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "findallId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/get-find-all-run-schema?${params}`, {
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
| `findallId` | string | yes | The Parallel FindAll run ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "enrichments": {
        "processor": "string"
      },
      "entity_type": "string",
      "generator": "string",
      "match_conditions": {
        "description": "string",
        "name": "Ava Chen"
      },
      "match_limit": 1,
      "objective": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `enrichments.processor` | string | Enrichment processor. |
| `entity_type` | string | Entity type being matched. |
| `generator` | string | Candidate generator. |
| `match_conditions.description` | string | Match condition description. |
| `match_conditions.name` | string | Match condition name. |
| `match_limit` | number | Maximum number of candidate matches. |
| `objective` | string | FindAll objective. |

## Native endpoint

Through the native Parallel Web Systems API, this operation is `GET /v1beta/findall/runs/:findall_id/schema` (base URL `https://api.parallel.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-find-all-run-schema.md) for the provider-specific parameters and requirements.

