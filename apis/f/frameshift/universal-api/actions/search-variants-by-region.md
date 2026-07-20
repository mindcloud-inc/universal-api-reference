# Frameshift: Search Variants By Region

Finds variants in Frameshift by genomic region.

```
GET https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/search-variants-by-region
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frameshift `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/search-variants-by-region?connectionId=$CONNECTION_ID&projectId=string&chr=string&start=1&end=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string",
  "chr": "string",
  "start": "1",
  "end": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/search-variants-by-region?${params}`, {
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
| `projectId` | string | yes | Resource identifier for the project to access |
| `chr` | string | yes | The chromosome to filter on. Use values like 1 rather than chr1. |
| `start` | number | yes | The region start to filter on. |
| `end` | number | yes | The region end to filter on. |
| `inheritance` | string | no | Optional inheritance filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "max_limit": 1,
      "project_has_variants": true,
      "query_status": "string",
      "removed_duplicates": true,
      "sqldebug": [
        "string"
      ],
      "variants": [
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
| `count` | number |  |
| `max_limit` | number |  |
| `project_has_variants` | boolean |  |
| `query_status` | string |  |
| `removed_duplicates` | boolean |  |
| `sqldebug` | array<string> |  |
| `variants` | array<object> |  |

## Native endpoint

Through the native Frameshift API, this operation is `GET /v1/projects/:project_id/variants/by-region` (base URL `https://mosaic.frameshift.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-variants-by-region.md) for the provider-specific parameters and requirements.

