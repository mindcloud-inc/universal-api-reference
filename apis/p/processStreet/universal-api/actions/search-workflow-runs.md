# Process Street: Search Workflow Runs



```
GET https://connect.mindcloud.co/v1/universal/processStreet/latest/actions/search-workflow-runs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Street `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processStreet/latest/actions/search-workflow-runs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processStreet/latest/actions/search-workflow-runs?${params}`, {
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
| `workflowId` | string | no | The ID of the workflow. |
| `name` | string | no | Filter workflow runs by partial name. |
| `status` | string | no | Filter by one or more workflow run statuses. Accepts multiple values in one string, delimited by `,`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "audit": {},
      "id": "string",
      "links": [
        {}
      ],
      "migrationStatus": "string",
      "name": "Ava Chen",
      "shared": true,
      "status": "string",
      "workflowId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `audit` | object |  |
| `id` | string |  |
| `links` | array<object> |  |
| `migrationStatus` | string |  |
| `name` | string |  |
| `shared` | boolean |  |
| `status` | string |  |
| `workflowId` | string |  |

## Native endpoint

Through the native Process Street API, this operation is `GET /workflow-runs` (base URL `https://public-api.process.st/api/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-workflow-runs.md) for the provider-specific parameters and requirements.

