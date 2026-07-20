# Zoho Projects: Get Issue Details

Retrieves issue details from Zoho Projects.

```
GET https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/get-issue-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Projects `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/get-issue-details?connectionId=$CONNECTION_ID&portalId=string&projectId=string&issueId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "portalId": "string",
  "projectId": "string",
  "issueId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/get-issue-details?${params}`, {
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
| `portalId` | string | yes | Zoho Projects portal ID. |
| `projectId` | string | yes | Zoho Projects project ID. |
| `issueId` | string | yes | Zoho Projects issue ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addedVia": "string",
      "assignee": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "lastName": "Chen",
        "name": "Ava Chen",
        "zpuid": "string",
        "zuid": 1
      },
      "classification": {
        "id": "string",
        "value": "string"
      },
      "createdBy": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "lastName": "Chen",
        "name": "Ava Chen",
        "zpuid": "string",
        "zuid": 1
      },
      "createdTime": "2026-05-07T12:00:00.000Z",
      "flag": "string",
      "id": "string",
      "isItReproducible": {
        "id": "string",
        "value": "string"
      },
      "lastUpdatedTime": "2026-05-07T12:00:00.000Z",
      "module": {
        "id": "string",
        "value": "string"
      },
      "name": "Ava Chen",
      "prefix": "string",
      "project": {
        "id": "string",
        "name": "Ava Chen"
      },
      "severity": {
        "id": "string",
        "value": "string"
      },
      "status": {
        "color": "string",
        "colorHexcode": "string",
        "id": "string",
        "isClosedType": true,
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addedVia` | string |  |
| `assignee.email` | string |  |
| `assignee.firstName` | string |  |
| `assignee.lastName` | string |  |
| `assignee.name` | string |  |
| `assignee.zpuid` | string |  |
| `assignee.zuid` | number |  |
| `classification.id` | string |  |
| `classification.value` | string |  |
| `createdBy.email` | string |  |
| `createdBy.firstName` | string |  |
| `createdBy.lastName` | string |  |
| `createdBy.name` | string |  |
| `createdBy.zpuid` | string |  |
| `createdBy.zuid` | number |  |
| `createdTime` | date |  |
| `flag` | string |  |
| `id` | string |  |
| `isItReproducible.id` | string |  |
| `isItReproducible.value` | string |  |
| `lastUpdatedTime` | date |  |
| `module.id` | string |  |
| `module.value` | string |  |
| `name` | string |  |
| `prefix` | string |  |
| `project.id` | string |  |
| `project.name` | string |  |
| `severity.id` | string |  |
| `severity.value` | string |  |
| `status.color` | string |  |
| `status.colorHexcode` | string |  |
| `status.id` | string |  |
| `status.isClosedType` | boolean |  |
| `status.name` | string |  |

## Native endpoint

Through the native Zoho Projects API, this operation is `GET /portal/[:PORTALID]/projects/[:PROJECTID]/issues/[:ISSUEID]` (base URL `https://projectsapi.zoho.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-issue-details.md) for the provider-specific parameters and requirements.

