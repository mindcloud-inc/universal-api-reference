# Productive.io: Get Workflow

Retrieves a workflow from your Productive.io account.

```
GET https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/get-workflow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Productive.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/get-workflow?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/get-workflow?${params}`, {
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
| `id` | string | yes | The Productive resource ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "archivedAt": "string",
        "name": "Ava Chen"
      },
      "id": "string",
      "relationships": {
        "organization": {
          "data": {
            "id": "string",
            "type": "string"
          }
        },
        "workflowStatuses": {
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
| `attributes.archivedAt` | string |  |
| `attributes.name` | string |  |
| `id` | string |  |
| `relationships.organization.data.id` | string |  |
| `relationships.organization.data.type` | string |  |
| `relationships.workflowStatuses.meta.included` | boolean |  |
| `type` | string |  |

## Native endpoint

Through the native Productive.io API, this operation is `GET /workflows/{{id}}` (base URL `https://api.productive.io/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-workflow.md) for the provider-specific parameters and requirements.

