# Productive.io: List Workflow Statuses

Retrieves workflow statuses from your Productive.io account.

```
GET https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/list-workflow-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productive.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/list-workflow-statuses?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/list-workflow-statuses?${params}`, {
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
      "attributes": {
        "categoryId": 1,
        "colorId": "string",
        "name": "Ava Chen",
        "position": 1
      },
      "id": "string",
      "relationships": {
        "organization": {
          "data": {
            "id": "string",
            "type": "string"
          }
        },
        "workflow": {
          "meta": {
            "included": true
          }
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.categoryId` | number |  |
| `attributes.colorId` | string |  |
| `attributes.name` | string |  |
| `attributes.position` | number |  |
| `id` | string |  |
| `relationships.organization.data.id` | string |  |
| `relationships.organization.data.type` | string |  |
| `relationships.workflow.meta.included` | boolean |  |
| `type` | string |  |

## Native endpoint

Through the native Productive.io API, this operation is `GET /workflow_statuses` (base URL `https://api.productive.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-workflow-statuses.md) for the provider-specific parameters and requirements.

