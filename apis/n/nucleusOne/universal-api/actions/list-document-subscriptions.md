# Nucleus One: List Document Subscriptions

Retrieves document subscriptions from a Nucleus One project.

```
GET https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/list-document-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nucleus One `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/list-document-subscriptions?connectionId=$CONNECTION_ID&organizationId=Enter%20organizationId&projectId=Enter%20projectId" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "Enter organizationId",
  "projectId": "Enter projectId"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/list-document-subscriptions?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "CreatedOn": "2026-05-07T12:00:00.000Z",
      "DocumentID": "string",
      "ModifiedOn": "2026-05-07T12:00:00.000Z",
      "OrganizationID": "string",
      "ProjectID": "string",
      "UserID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CreatedOn` | date |  |
| `DocumentID` | string |  |
| `ModifiedOn` | date |  |
| `OrganizationID` | string |  |
| `ProjectID` | string |  |
| `UserID` | string |  |

## Native endpoint

Through the native Nucleus One API, this operation is `GET /organizations/:organizationId/projects/:projectId/documentSubscriptions` (base URL `https://client-api.nucleus.one/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-document-subscriptions.md) for the provider-specific parameters and requirements.

