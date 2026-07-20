# NeetoForm: List Submissions

Retrieves submissions for a NeetoForm form.

```
GET https://connect.mindcloud.co/v1/universal/neetoForm/latest/actions/list-submissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NeetoForm `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/neetoForm/latest/actions/list-submissions?connectionId=$CONNECTION_ID&limit=25&offset=0&formId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "formId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/neetoForm/latest/actions/list-submissions?${params}`, {
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
| `formId` | string | yes | Unique ID of the form whose submissions you want to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {
        "currentPageNumber": 1,
        "pageSize": 1,
        "totalPages": 1,
        "totalRecords": 1
      },
      "submissions": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "responses": [
            {
              "id": "string",
              "kind": "string",
              "label": "string",
              "position": 1,
              "slug": "string",
              "value": "string"
            }
          ],
          "userAgent": {
            "createdAt": "2026-05-07T12:00:00.000Z",
            "deviceName": "Ava Chen",
            "deviceType": "string",
            "id": "string",
            "ipAddress": "string",
            "name": "Ava Chen",
            "operatingSystem": "string",
            "operatingSystemVersion": "string",
            "submissionId": "string",
            "updatedAt": "2026-05-07T12:00:00.000Z",
            "version": "string"
          }
        }
      ],
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination.currentPageNumber` | number |  |
| `pagination.pageSize` | number |  |
| `pagination.totalPages` | number |  |
| `pagination.totalRecords` | number |  |
| `submissions[].createdAt` | date |  |
| `submissions[].id` | string |  |
| `submissions[].responses[].id` | string |  |
| `submissions[].responses[].kind` | string |  |
| `submissions[].responses[].label` | string |  |
| `submissions[].responses[].position` | number |  |
| `submissions[].responses[].slug` | string |  |
| `submissions[].responses[].value` | string |  |
| `submissions[].userAgent.createdAt` | date |  |
| `submissions[].userAgent.deviceName` | string |  |
| `submissions[].userAgent.deviceType` | string |  |
| `submissions[].userAgent.id` | string |  |
| `submissions[].userAgent.ipAddress` | string |  |
| `submissions[].userAgent.name` | string |  |
| `submissions[].userAgent.operatingSystem` | string |  |
| `submissions[].userAgent.operatingSystemVersion` | string |  |
| `submissions[].userAgent.submissionId` | string |  |
| `submissions[].userAgent.updatedAt` | date |  |
| `submissions[].userAgent.version` | string |  |
| `totalCount` | number |  |

## Native endpoint

Through the native NeetoForm API, this operation is `GET /forms/:form_id/submissions` (base URL `https://{{credentials.workspaceSubdomain}}.neetoform.com/api/external/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-submissions.md) for the provider-specific parameters and requirements.

