# Griptape: List Tools

Finds tools in Griptape.

```
GET https://connect.mindcloud.co/v1/universal/griptape/latest/actions/list-tools
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Griptape `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/griptape/latest/actions/list-tools?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/griptape/latest/actions/list-tools?${params}`, {
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
      "tools": [
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
            "string"
          ],
          "latest_deployment_id": "string",
          "name": "Ava Chen",
          "organization_id": "string",
          "tool_config_file": "string",
          "tool_id": "string",
          "updated_at": "string"
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
| `tools[].code.github.name` | string |  |
| `tools[].code.github.owner` | string |  |
| `tools[].code.github.push.branch` | string |  |
| `tools[].code.github.push.tag` | string |  |
| `tools[].created_at` | string |  |
| `tools[].created_by` | string |  |
| `tools[].description` | string |  |
| `tools[].env_vars` | array |  |
| `tools[].latest_deployment_id` | string |  |
| `tools[].name` | string |  |
| `tools[].organization_id` | string |  |
| `tools[].tool_config_file` | string |  |
| `tools[].tool_id` | string |  |
| `tools[].updated_at` | string |  |

## Native endpoint

Through the native Griptape API, this operation is `GET /api/tools` (base URL `https://cloud.griptape.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tools.md) for the provider-specific parameters and requirements.

