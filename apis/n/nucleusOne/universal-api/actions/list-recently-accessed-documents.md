# Nucleus One: List Recently Accessed Documents

Retrieves recently accessed documents from a Nucleus One organization.

```
GET https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/list-recently-accessed-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nucleus One `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/list-recently-accessed-documents?connectionId=$CONNECTION_ID&organizationId=Enter%20organizationId" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "Enter organizationId"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/list-recently-accessed-documents?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cursor` | string | no | Pagination cursor Example: `Paste a cursor from a previous response`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "AccessedOn": "2026-05-07T12:00:00.000Z",
      "DocumentID": "string",
      "DocumentName": "Ava Chen",
      "ID": "string",
      "OrganizationID": "string",
      "OrganizationMemberID": "string",
      "ProjectID": "string",
      "ProjectName": "Ava Chen",
      "UniqueID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AccessedOn` | date |  |
| `DocumentID` | string |  |
| `DocumentName` | string |  |
| `ID` | string |  |
| `OrganizationID` | string |  |
| `OrganizationMemberID` | string |  |
| `ProjectID` | string |  |
| `ProjectName` | string |  |
| `UniqueID` | string |  |

## Native endpoint

Through the native Nucleus One API, this operation is `GET /organizations/:organizationId/recentlyAccessedDocuments` (base URL `https://client-api.nucleus.one/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-recently-accessed-documents.md) for the provider-specific parameters and requirements.

