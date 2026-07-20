# Leantime: List Projects



```
GET https://connect.mindcloud.co/v1/universal/leantime/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leantime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leantime/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leantime/latest/actions/list-projects?${params}`, {
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
| `params.showClosedProjects` | boolean | no | Include closed projects in the response. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientId": {},
      "clientName": {},
      "details": "string",
      "dollarBudget": 1,
      "end": {},
      "hourBudget": "string",
      "id": 1,
      "isFavorite": 1,
      "menuType": "string",
      "modified": "string",
      "name": "Ava Chen",
      "parent": {},
      "parentId": {},
      "parentName": {},
      "start": {},
      "state": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientId` | object |  |
| `clientName` | object |  |
| `details` | string |  |
| `dollarBudget` | number |  |
| `end` | object |  |
| `hourBudget` | string |  |
| `id` | number |  |
| `isFavorite` | number |  |
| `menuType` | string |  |
| `modified` | string |  |
| `name` | string |  |
| `parent` | object |  |
| `parentId` | object |  |
| `parentName` | object |  |
| `start` | object |  |
| `state` | object |  |
| `type` | string |  |

## Native endpoint

Through the native Leantime API, this operation is `POST /` (base URL `{{credentials.workspaceUrl}}/api/jsonrpc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

