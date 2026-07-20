# Billetto: List Target Group Imports By Target Group

Retrieves target group imports from Billetto by target group.

```
GET https://connect.mindcloud.co/v1/universal/billetto/latest/actions/list-target-group-imports-by-target-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billetto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billetto/latest/actions/list-target-group-imports-by-target-group?connectionId=$CONNECTION_ID&target_group=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "target_group": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billetto/latest/actions/list-target-group-imports-by-target-group?${params}`, {
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
| `target_group` | string | yes | Required target group ID to list imports for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "data": [
        {}
      ],
      "has_more": true,
      "id": "string",
      "object": "string",
      "size": 1,
      "status": "string",
      "target_group": "string",
      "total": 1,
      "updated_at": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string | Import creation timestamp. |
| `data` | array<object> | Target group import records. |
| `has_more` | boolean | Whether additional import records are available. |
| `id` | string | Import identifier from list items. |
| `object` | string | Response object type. |
| `size` | number | Number of imported members. |
| `status` | string | Import status. |
| `target_group` | string | Target group identifier from list items. |
| `total` | number | Total number of import records. |
| `updated_at` | string | Import update timestamp. |
| `url` | string | Canonical URL for the list response. |

## Native endpoint

Through the native Billetto API, this operation is `GET organiser/target_group_imports` (base URL `https://billetto.dk/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-target-group-imports-by-target-group.md) for the provider-specific parameters and requirements.

