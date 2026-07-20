# TalentHR: List Employee Custom Fields

Retrieves an employee's custom fields from TalentHR.

```
GET https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/list-employee-custom-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TalentHR `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/list-employee-custom-fields?connectionId=$CONNECTION_ID&employee=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "employee": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/talentHR/latest/actions/list-employee-custom-fields?${params}`, {
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
| `employee` | number | yes | TalentHR employee ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alwaysActive": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customFieldType": {},
      "customFieldTypeId": 1,
      "customFieldValues": [
        {}
      ],
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "expirationId": 1,
      "fieldName": "Ava Chen",
      "form": "string",
      "hasMultipleRecords": true,
      "id": 1,
      "isEditable": 1,
      "isEnabled": true,
      "isGroup": true,
      "isPredefined": true,
      "modelBy": "string",
      "name": "Ava Chen",
      "parentGroupId": 1,
      "slug": "string",
      "subfields": 1,
      "subfieldsNames": [
        {}
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "visibleTo": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alwaysActive` | number |  |
| `createdAt` | date |  |
| `customFieldType` | object |  |
| `customFieldTypeId` | number |  |
| `customFieldValues` | array<object> |  |
| `deletedAt` | date |  |
| `expirationId` | number |  |
| `fieldName` | string |  |
| `form` | string |  |
| `hasMultipleRecords` | boolean |  |
| `id` | number |  |
| `isEditable` | number |  |
| `isEnabled` | boolean |  |
| `isGroup` | boolean |  |
| `isPredefined` | boolean |  |
| `modelBy` | string |  |
| `name` | string |  |
| `parentGroupId` | number |  |
| `slug` | string |  |
| `subfields` | number |  |
| `subfieldsNames` | array<object> |  |
| `updatedAt` | date |  |
| `visibleTo` | string |  |

## Native endpoint

Through the native TalentHR API, this operation is `GET /employees/:employee/custom-fields` (base URL `https://pubapi.talenthr.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-employee-custom-fields.md) for the provider-specific parameters and requirements.

