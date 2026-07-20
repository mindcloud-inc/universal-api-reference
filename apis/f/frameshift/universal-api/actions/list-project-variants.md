# Frameshift: List Project Variants

Retrieves a list of project variants from Frameshift.

```
GET https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/list-project-variants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frameshift `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/list-project-variants?connectionId=$CONNECTION_ID&limit=25&offset=0&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/list-project-variants?${params}`, {
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
| `search` | string | no | The search keyword to filter the results by |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alt": "string",
      "chr": "string",
      "id": 1,
      "length": 1,
      "r_end": 1,
      "r_start": 1,
      "ref": "string",
      "var_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alt` | string |  |
| `chr` | string |  |
| `id` | number |  |
| `length` | number |  |
| `r_end` | number |  |
| `r_start` | number |  |
| `ref` | string |  |
| `var_type` | string |  |

## Native endpoint

Through the native Frameshift API, this operation is `GET /v1/projects/:project_id/variants/list` (base URL `https://mosaic.frameshift.io/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-project-variants.md) for the provider-specific parameters and requirements.

