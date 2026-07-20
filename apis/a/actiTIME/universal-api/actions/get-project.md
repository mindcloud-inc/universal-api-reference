# actiTIME: Get Project

Retrieves a specific project from actiTIME.

```
GET https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a actiTIME `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/get-project?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/get-project?${params}`, {
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
| `id` | number | yes | Project identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowedActions": {
        "canDelete": true,
        "canModify": true
      },
      "archived": true,
      "created": "2026-05-07T12:00:00.000Z",
      "customerId": 1,
      "customerName": "Ava Chen",
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowedActions.canDelete` | boolean | Whether the project can be deleted. |
| `allowedActions.canModify` | boolean | Whether the project can be modified. |
| `archived` | boolean | Whether the project is archived. |
| `created` | date | Creation date and time. |
| `customerId` | number | Customer identifier. |
| `customerName` | string | Customer name. |
| `description` | string | Project description. |
| `id` | number | Unique project identifier. |
| `name` | string | Project name. |
| `url` | string | Project URL. |

## Native endpoint

Through the native actiTIME API, this operation is `GET /projects/:id` (base URL `{{credentials.instanceUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

