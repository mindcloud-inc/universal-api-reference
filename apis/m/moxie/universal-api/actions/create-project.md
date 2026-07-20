# Moxie: Create Project

Creates a new project in Moxie.

```
POST https://connect.mindcloud.co/v1/universal/moxie/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moxie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moxie/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "clientName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moxie/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "clientName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Project name. |
| `clientName` | string | yes | Existing client name for the project. |
| `templateName` | string | no | Project template name to clone from. |
| `startDate` | date | no | Project start date. |
| `dueDate` | date | no | Project due date. |
| `portalAccess` | string | no | Portal access level for the project. |
| `showTimeWorkedInPortal` | boolean | no | Whether time worked should be visible in the client portal. |
| `feeSchedule` | object | no | Fee schedule object when not using a template. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "active": true,
      "clientId": "string",
      "clientMini": {},
      "customValues": [
        {}
      ],
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "feeSchedule": {},
      "id": "string",
      "invoiceIds": [
        "string"
      ],
      "name": "Ava Chen",
      "portalAccess": "string",
      "projectTypeId": "string",
      "sampleData": true,
      "showTimeWorkedInPortal": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `active` | boolean |  |
| `clientId` | string |  |
| `clientMini` | object |  |
| `customValues` | array<object> |  |
| `dateCreated` | date |  |
| `description` | string |  |
| `feeSchedule` | object |  |
| `id` | string |  |
| `invoiceIds` | array<string> |  |
| `name` | string |  |
| `portalAccess` | string |  |
| `projectTypeId` | string |  |
| `sampleData` | boolean |  |
| `showTimeWorkedInPortal` | boolean |  |

## Native endpoint

Through the native Moxie API, this operation is `POST /action/projects/create` (base URL `https://pod01.withmoxie.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

