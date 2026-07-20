# Clockify: List Project Custom Fields

Lists all project custom fields in Clockify.

```
GET https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-project-custom-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-project-custom-fields?connectionId=$CONNECTION_ID&workspaceId=string&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string",
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/list-project-custom-fields?${params}`, {
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
| `workspaceId` | list<string> | yes |  |
| `projectId` | string<string> | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `entityType` | string | no | Example: `STANDARD`. |
| `status` | list<string> | no | One of: `INACTIVE`, `INVISIBLE`, `VISIBLE`. Example: `ACTIVE`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowedValues": [
        [
          "string"
        ]
      ],
      "description": "string",
      "entityType": "string",
      "id": "string",
      "name": "Ava Chen",
      "onlyAdminCanEdit": true,
      "placeholder": "string",
      "projectDefaultValues": [
        [
          {}
        ]
      ],
      "required": true,
      "status": "string",
      "type": "string",
      "workspaceDefaultValue": {},
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowedValues[]` | array<string> |  |
| `description` | string |  |
| `entityType` | string |  |
| `id` | string |  |
| `name` | string |  |
| `onlyAdminCanEdit` | boolean |  |
| `placeholder` | string |  |
| `projectDefaultValues[]` | array<object> |  |
| `projectDefaultValues[].projectId` | string |  |
| `projectDefaultValues[].status` | string |  |
| `projectDefaultValues[].value` | object |  |
| `required` | boolean |  |
| `status` | string |  |
| `type` | string |  |
| `workspaceDefaultValue` | object |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Clockify API, this operation is `GET workspaces/:workspaceId/projects/:projectId/custom-fields` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-custom-fields.md) for the provider-specific parameters and requirements.

