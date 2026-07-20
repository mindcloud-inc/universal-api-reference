# Clockify: Update Workspace Custom Field

Updates a workspace custom field in Clockify.

```
PUT https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-workspace-custom-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-workspace-custom-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "customFieldId": "string",
  "name": "Example Name",
  "type": "STANDARD"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-workspace-custom-field', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "customFieldId": "string",
    "name": "Example Name",
    "type": "STANDARD"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | list<string> | yes |  |
| `customFieldId` | string<string> | yes |  |
| `name` | string | yes | Example: `Example Name`. |
| `type` | list<string> | yes | One of: `CHECKBOX`, `DROPDOWN_MULTIPLE`, `DROPDOWN_SINGLE`, `LINK`, `NUMBER`, `TXT`. Example: `STANDARD`. |
| `allowedValues[]` | array<string> | no |  |
| `description` | string | no | Example: `Example description`. |
| `onlyAdminCanEdit` | boolean | no | Example: `true`. |
| `placeholder` | string | no |  |
| `required` | boolean | no | Example: `true`. |
| `status` | list<string> | no | One of: `INACTIVE`, `INVISIBLE`, `VISIBLE`. Example: `ACTIVE`. |
| `workspaceDefaultValue` | object | no |  |

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

Through the native Clockify API, this operation is `PUT workspaces/:workspaceId/custom-fields/:customFieldId` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-workspace-custom-field.md) for the provider-specific parameters and requirements.

