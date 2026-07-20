# Float: List Logged Time

Retrieves logged time entries from Float.

```
GET https://connect.mindcloud.co/v1/universal/float/latest/actions/list-logged-time
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Float `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/float/latest/actions/list-logged-time?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/float/latest/actions/list-logged-time?${params}`, {
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
| `endDate` | string | no | End of date range in format YYYY-MM-DD |
| `fields` | string | no | Comma-delimited set of fields to include in the response |
| `modifiedSince` | string | no | Filter on records with an equal or later modified timestamp |
| `peopleId` | number | no | A people ID to filter the response on |
| `phaseId` | string | no | A phase ID associated with a project to filter the response on |
| `startDate` | string | no | Start of date range in format YYYY-MM-DD |
| `taskMetaId` | string | no | A project task ID to filter the response on |
| `projectId` | number | no | A project ID to filter the response on |
| `phaseId` | number | no | A phase ID associated with a project to filter the response on |
| `taskMetaId` | number | no | A project task ID to filter the response on |
| `startDate` | string | no | Start of date range in format YYYY-MM-DD |
| `endDate` | string | no | End of date range in format YYYY-MM-DD |
| `modifiedSince` | string | no | Filter on records with an equal or later modified timestamp |
| `fields` | string | no | Comma-delimited set of fields to include in the response |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billable": 1,
      "created": "string",
      "createdBy": 1,
      "date": "string",
      "hours": 1,
      "locked": 1,
      "lockedDate": {},
      "loggedTimeId": "string",
      "modified": "string",
      "modifiedBy": 1,
      "notes": "string",
      "peopleId": 1,
      "phaseId": 1,
      "priority": 1,
      "projectId": 1,
      "referenceDate": {},
      "taskId": 1,
      "taskMetaId": 1,
      "taskName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billable` | number |  |
| `created` | string |  |
| `createdBy` | number |  |
| `date` | string |  |
| `hours` | number |  |
| `locked` | number |  |
| `lockedDate` | object |  |
| `loggedTimeId` | string |  |
| `modified` | string |  |
| `modifiedBy` | number |  |
| `notes` | string |  |
| `peopleId` | number |  |
| `phaseId` | number |  |
| `priority` | number |  |
| `projectId` | number |  |
| `referenceDate` | object |  |
| `taskId` | number |  |
| `taskMetaId` | number |  |
| `taskName` | string |  |

## Native endpoint

Through the native Float API, this operation is `GET /logged-time` (base URL `https://api.float.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-logged-time.md) for the provider-specific parameters and requirements.

