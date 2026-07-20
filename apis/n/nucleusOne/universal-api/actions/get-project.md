# Nucleus One: Get Project

Retrieves a project from Nucleus One.

```
GET https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nucleus One `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/get-project?connectionId=$CONNECTION_ID&organizationId=Enter%20organizationId&projectId=Enter%20projectId" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "Enter organizationId",
  "projectId": "Enter projectId"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nucleusOne/latest/actions/get-project?${params}`, {
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
| `organizationId` | string | yes | Organization ID Example: `Enter organizationId`. |
| `projectId` | string | yes | Project ID Example: `Enter projectId`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "$schema": "string",
      "Access": {},
      "AccessModifiedOn": "2026-05-07T12:00:00.000Z",
      "AccessType": "string",
      "AccessTypeModifiedOn": "2026-05-07T12:00:00.000Z",
      "CreatedByUserEmail": "ava@example.com",
      "CreatedByUserID": "string",
      "CreatedByUserName": "Ava Chen",
      "CreatedOn": "2026-05-07T12:00:00.000Z",
      "Disabled": true,
      "ID": "string",
      "IsMarkedForPurge": true,
      "Name": "Ava Chen",
      "NameLower": "Ava Chen",
      "OrganizationID": "string",
      "PurgeMarkedByUserEmail": "ava@example.com",
      "PurgeMarkedByUserID": "string",
      "PurgeMarkedByUserName": "Ava Chen",
      "PurgeMarkedOn": "2026-05-07T12:00:00.000Z",
      "SourceContentCopy": true,
      "SourceID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `$schema` | string |  |
| `Access` | object |  |
| `AccessModifiedOn` | date |  |
| `AccessType` | string |  |
| `AccessTypeModifiedOn` | date |  |
| `CreatedByUserEmail` | string |  |
| `CreatedByUserID` | string |  |
| `CreatedByUserName` | string |  |
| `CreatedOn` | date |  |
| `Disabled` | boolean |  |
| `ID` | string |  |
| `IsMarkedForPurge` | boolean |  |
| `Name` | string |  |
| `NameLower` | string |  |
| `OrganizationID` | string |  |
| `PurgeMarkedByUserEmail` | string |  |
| `PurgeMarkedByUserID` | string |  |
| `PurgeMarkedByUserName` | string |  |
| `PurgeMarkedOn` | date |  |
| `SourceContentCopy` | boolean |  |
| `SourceID` | string |  |

## Native endpoint

Through the native Nucleus One API, this operation is `GET /organizations/:organizationId/projects/:projectId` (base URL `https://client-api.nucleus.one/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

