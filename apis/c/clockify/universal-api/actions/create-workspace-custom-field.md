# Clockify: Create Workspace Custom Field

Creates a workspace custom field in Clockify.

```
POST https://connect.mindcloud.co/v1/universal/clockify/latest/actions/create-workspace-custom-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/create-workspace-custom-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "name": "Example Name",
  "type": "STANDARD"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clockify/latest/actions/create-workspace-custom-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
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
| `name` | string | yes | Example: `Example Name`. |
| `type` | list<string> | yes | One of: `CHECKBOX`, `DROPDOWN_MULTIPLE`, `DROPDOWN_SINGLE`, `LINK`, `NUMBER`, `TXT`. Example: `STANDARD`. |
| `allowedValues[]` | array<string> | no |  |
| `description` | string | no | Example: `Example description`. |
| `entityType` | list<string> | no | One of: `TIMEENTRY`, `USER`. Example: `STANDARD`. |
| `onlyAdminCanEdit` | boolean | no | Example: `true`. |
| `placeholder` | string | no |  |
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

Through the native Clockify API, this operation is `POST workspaces/:workspaceId/custom-fields` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-workspace-custom-field.md) for the provider-specific parameters and requirements.

