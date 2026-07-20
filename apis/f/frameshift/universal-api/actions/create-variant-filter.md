# Frameshift: Create Variant Filter

Creates a variant filter in Frameshift.

```
POST https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/create-variant-filter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Frameshift `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/create-variant-filter" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "name": "Ava Chen",
  "filter": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/frameshift/latest/actions/create-variant-filter', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "name": "Ava Chen",
    "filter": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | Resource identifier for the project to access |
| `name` | string | yes | Name for the variant filter |
| `description` | string | no | Description of the variant filter |
| `filter` | object | yes | JSON describing the variant filters |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "filter": {
        "var_type": [
          "string"
        ]
      },
      "id": 1,
      "name": "Ava Chen",
      "project_id": 1,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string |  |
| `created_at` | date |  |
| `description` | string |  |
| `filter.var_type[]` | string |  |
| `id` | number |  |
| `name` | string |  |
| `project_id` | number |  |
| `updated_at` | date |  |
| `user_id` | number |  |

## Native endpoint

Through the native Frameshift API, this operation is `POST /v1/projects/:project_id/variants/filters` (base URL `https://mosaic.frameshift.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-variant-filter.md) for the provider-specific parameters and requirements.

