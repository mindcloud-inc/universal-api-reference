# Clockify: Remove Project Custom Field

Removes a project custom field in Clockify.

```
DELETE https://connect.mindcloud.co/v1/universal/clockify/latest/actions/remove-project-custom-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/remove-project-custom-field?connectionId=$CONNECTION_ID&workspaceId=string&projectId=string&customFieldId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string",
  "projectId": "string",
  "customFieldId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/remove-project-custom-field?${params}`, {
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
| `customFieldId` | string<string> | yes |  |

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

Through the native Clockify API, this operation is `DELETE workspaces/:workspaceId/projects/:projectId/custom-fields/:customFieldId` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-project-custom-field.md) for the provider-specific parameters and requirements.

