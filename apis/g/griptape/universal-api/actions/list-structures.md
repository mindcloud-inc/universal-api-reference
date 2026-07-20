# Griptape: List Structures

Finds structures in Griptape.

```
GET https://connect.mindcloud.co/v1/universal/griptape/latest/actions/list-structures
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Griptape `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/griptape/latest/actions/list-structures?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/griptape/latest/actions/list-structures?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {
        "page_number": 1,
        "page_size": 1,
        "total_count": 1,
        "total_pages": 1
      },
      "structures": [
        {
          "code": {
            "github": {
              "name": "Ava Chen",
              "owner": "string",
              "push": {
                "branch": "string",
                "tag": "string"
              }
            }
          },
          "created_at": "string",
          "created_by": "string",
          "description": "string",
          "env_vars": [
            {
              "name": "Ava Chen",
              "source": "string",
              "value": "string"
            }
          ],
          "latest_deployment_id": "string",
          "name": "Ava Chen",
          "organization_id": "string",
          "structure_config_file": "string",
          "structure_id": "string",
          "updated_at": "string",
          "webhook_enabled": true
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination.page_number` | number |  |
| `pagination.page_size` | number |  |
| `pagination.total_count` | number |  |
| `pagination.total_pages` | number |  |
| `structures[].code.github.name` | string |  |
| `structures[].code.github.owner` | string |  |
| `structures[].code.github.push.branch` | string |  |
| `structures[].code.github.push.tag` | string |  |
| `structures[].created_at` | string |  |
| `structures[].created_by` | string |  |
| `structures[].description` | string |  |
| `structures[].env_vars[].name` | string |  |
| `structures[].env_vars[].source` | string |  |
| `structures[].env_vars[].value` | string |  |
| `structures[].latest_deployment_id` | string |  |
| `structures[].name` | string |  |
| `structures[].organization_id` | string |  |
| `structures[].structure_config_file` | string |  |
| `structures[].structure_id` | string |  |
| `structures[].updated_at` | string |  |
| `structures[].webhook_enabled` | boolean |  |

## Native endpoint

Through the native Griptape API, this operation is `GET /api/structures` (base URL `https://cloud.griptape.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-structures.md) for the provider-specific parameters and requirements.

