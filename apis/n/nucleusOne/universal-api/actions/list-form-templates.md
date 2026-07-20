# Nucleus One: List Form Templates

Retrieves form templates from a Nucleus One project.

```
GET https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/list-form-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nucleus One `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/list-form-templates?connectionId=$CONNECTION_ID&organizationId=Enter%20organizationId&projectId=Enter%20projectId" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "Enter organizationId",
  "projectId": "Enter projectId"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/list-form-templates?${params}`, {
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
| `cursor` | string | no | Pagination cursor. Leave empty to get the first page of results. Example: `Paste a cursor from a previous response`. |
| `pageSize` | number | no | Number of items per page Example: `Enter pageSize`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$schema": "string",
      "Aspect": 1,
      "AssetItemTagAssetItemIDs": [
        "string"
      ],
      "AssetItemTags": [
        {}
      ],
      "CreatedOn": "2026-05-07T12:00:00.000Z",
      "DisableSnapToGrid": true,
      "FormTemplateSourceFailedProcessing": true,
      "FormTemplateSourceID": "string",
      "FormTemplateSourceIsImported": true,
      "ID": "string",
      "IsPublic": true,
      "Name": "Ava Chen",
      "NameLower": "Ava Chen",
      "OrganizationID": "string",
      "PageCount": 1,
      "PageHeight": 1,
      "Pages": [
        {}
      ],
      "PageSize": "string",
      "PageWidth": 1,
      "ProjectAccess": {},
      "ProjectID": "string",
      "ProjectName": "Ava Chen",
      "RenderType": "string",
      "Tags": [
        "string"
      ],
      "UniqueID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$schema` | string |  |
| `Aspect` | number |  |
| `AssetItemTagAssetItemIDs` | array<string> |  |
| `AssetItemTags` | array<object> |  |
| `CreatedOn` | date |  |
| `DisableSnapToGrid` | boolean |  |
| `FormTemplateSourceFailedProcessing` | boolean |  |
| `FormTemplateSourceID` | string |  |
| `FormTemplateSourceIsImported` | boolean |  |
| `ID` | string |  |
| `IsPublic` | boolean |  |
| `Name` | string |  |
| `NameLower` | string |  |
| `OrganizationID` | string |  |
| `PageCount` | number |  |
| `PageHeight` | number |  |
| `Pages` | array<object> |  |
| `PageSize` | string |  |
| `PageWidth` | number |  |
| `ProjectAccess` | object |  |
| `ProjectID` | string |  |
| `ProjectName` | string |  |
| `RenderType` | string |  |
| `Tags` | array<string> |  |
| `UniqueID` | string |  |

## Native endpoint

Through the native Nucleus One API, this operation is `GET /organizations/:organizationId/projects/:projectId/formTemplates` (base URL `https://client-api.nucleus.one/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-form-templates.md) for the provider-specific parameters and requirements.

