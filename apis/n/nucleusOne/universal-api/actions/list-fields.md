# Nucleus One: List Fields

Retrieves project fields from Nucleus One.

```
GET https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/list-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nucleus One `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/list-fields?connectionId=$CONNECTION_ID&organizationId=Enter%20organizationId&projectId=Enter%20projectId" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "Enter organizationId",
  "projectId": "Enter projectId"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/list-fields?${params}`, {
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
| `organizationId` | string | yes | ID of the organization Example: `Enter organizationId`. |
| `projectId` | string | yes | ID of the project Example: `Enter projectId`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `getAll` | string | no | If true, returns all results without pagination Example: `Enter getAll`. |
| `cursor` | string | no | Pagination cursor Example: `Paste a cursor from a previous response`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$schema": "string",
      "AllowMultipleLines": true,
      "AllowMultipleValues": true,
      "AllowNewSelectionListItems": true,
      "ChildFieldIDs": [
        "string"
      ],
      "CreatedOn": "2026-05-07T12:00:00.000Z",
      "DecimalPlaces": 1,
      "DisplaySelectionList": true,
      "DocumentTags": [
        "string"
      ],
      "HideLabel": true,
      "ID": "string",
      "Label": "string",
      "LabelLower": "string",
      "LabelOrName": "Ava Chen",
      "LabelOrNameLower": "Ava Chen",
      "Mask": "string",
      "Name": "Ava Chen",
      "NameLower": "Ava Chen",
      "OrganizationID": "string",
      "ParentFieldID": "string",
      "ProjectAccess": {},
      "ProjectID": "string",
      "ProjectName": "Ava Chen",
      "Rank": 1,
      "ReadOnly": true,
      "Required": true,
      "Rows": 1,
      "SaveNewSelectionListItems": true,
      "SelectionListIsDependent": true,
      "Sensitive": true,
      "SourceID": "string",
      "TextMatchType": "string",
      "Type": "string",
      "UseCreationDate": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$schema` | string |  |
| `AllowMultipleLines` | boolean |  |
| `AllowMultipleValues` | boolean |  |
| `AllowNewSelectionListItems` | boolean |  |
| `ChildFieldIDs` | array<string> |  |
| `CreatedOn` | date |  |
| `DecimalPlaces` | number |  |
| `DisplaySelectionList` | boolean |  |
| `DocumentTags` | array<string> |  |
| `HideLabel` | boolean |  |
| `ID` | string |  |
| `Label` | string |  |
| `LabelLower` | string |  |
| `LabelOrName` | string |  |
| `LabelOrNameLower` | string |  |
| `Mask` | string |  |
| `Name` | string |  |
| `NameLower` | string |  |
| `OrganizationID` | string |  |
| `ParentFieldID` | string |  |
| `ProjectAccess` | object |  |
| `ProjectID` | string |  |
| `ProjectName` | string |  |
| `Rank` | number |  |
| `ReadOnly` | boolean |  |
| `Required` | boolean |  |
| `Rows` | number |  |
| `SaveNewSelectionListItems` | boolean |  |
| `SelectionListIsDependent` | boolean |  |
| `Sensitive` | boolean |  |
| `SourceID` | string |  |
| `TextMatchType` | string |  |
| `Type` | string |  |
| `UseCreationDate` | boolean |  |

## Native endpoint

Through the native Nucleus One API, this operation is `GET /organizations/:organizationId/projects/:projectId/fields` (base URL `https://client-api.nucleus.one/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-fields.md) for the provider-specific parameters and requirements.

