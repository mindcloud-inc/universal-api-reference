# Nucleus One: List Recent Document Signature Forms

Retrieves recent document signature forms from Nucleus One.

```
GET https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/list-recent-document-signature-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nucleus One `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/list-recent-document-signature-forms?connectionId=$CONNECTION_ID&organizationId=Enter%20organizationId&projectId=Enter%20projectId" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "Enter organizationId",
  "projectId": "Enter projectId"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/list-recent-document-signature-forms?${params}`, {
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
| `nameFilter` | string | no | Filter forms by name Example: `Enter nameFilter`. |
| `excludingId` | string | no | Exclude form with this ID from results Example: `Enter excludingId`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$schema": "string",
      "CreatedOn": "2026-05-07T12:00:00.000Z",
      "DocumentID": "string",
      "DocumentName": "Ava Chen",
      "DocumentNameLower": "Ava Chen",
      "HasFormFields": true,
      "ID": "string",
      "LastViewedPageIndex": 1,
      "OrganizationID": "string",
      "ProjectID": "string",
      "SignatureFormTemplateID": "string",
      "TotalFormFields": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$schema` | string |  |
| `CreatedOn` | date |  |
| `DocumentID` | string |  |
| `DocumentName` | string |  |
| `DocumentNameLower` | string |  |
| `HasFormFields` | boolean |  |
| `ID` | string |  |
| `LastViewedPageIndex` | number |  |
| `OrganizationID` | string |  |
| `ProjectID` | string |  |
| `SignatureFormTemplateID` | string |  |
| `TotalFormFields` | number |  |

## Native endpoint

Through the native Nucleus One API, this operation is `GET /organizations/:organizationId/projects/:projectId/recentDocumentSignatureForms` (base URL `https://client-api.nucleus.one/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-recent-document-signature-forms.md) for the provider-specific parameters and requirements.

