# Frameshift: List Variant Sets

Retrieves a list of variant sets from Frameshift.

```
GET https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/list-variant-sets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frameshift `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/list-variant-sets?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/list-variant-sets?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "clinvar_annotation_version_id_a": 1,
      "clinvar_annotation_version_id_b": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "is_public_to_project": true,
      "is_watchlist": true,
      "name": "Ava Chen",
      "project_id": 1,
      "selected_variant_annotation_version_ids": [
        1
      ],
      "updated_at": "2026-05-07T12:00:00.000Z",
      "user_id": 1,
      "user": {
        "first_name": "Ava",
        "id": 1,
        "last_name": "Chen",
        "username": "Ava Chen"
      },
      "variant_count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clinvar_annotation_version_id_a` | number |  |
| `clinvar_annotation_version_id_b` | number |  |
| `created_at` | date |  |
| `description` | string |  |
| `id` | number |  |
| `is_public_to_project` | boolean |  |
| `is_watchlist` | boolean |  |
| `name` | string |  |
| `project_id` | number |  |
| `selected_variant_annotation_version_ids` | array<number> |  |
| `updated_at` | date |  |
| `user_id` | number |  |
| `user.first_name` | string |  |
| `user.id` | number |  |
| `user.last_name` | string |  |
| `user.username` | string |  |
| `variant_count` | number |  |

## Native endpoint

Through the native Frameshift API, this operation is `GET /v1/projects/:project_id/variants/sets` (base URL `https://mosaic.frameshift.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-variant-sets.md) for the provider-specific parameters and requirements.

