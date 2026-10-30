# GoCanvas: List Submissions



```
GET https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/list-submissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCanvas `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/list-submissions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/list-submissions?${params}`, {
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
| `formId` | number | no | Filter by form; at least one of Form ID, User ID, or User Email is required. |
| `userId` | number | no | Do not combine with User Email. |
| `userEmail` | string | no | Do not combine with User ID. |
| `departmentId` | number | no | Defaults to the user's default department. |
| `status` | list | no | Defaults to completed. One of: `all`, `assigned`, `completed`, `custom`, `deleted`, `handed-off`, `in-progress`, `overdue`, `rejected`, `saved-to-cloud`, `unassigned`, `unfinished`. |
| `handOff` | string | no | Required when Status is handed-off. |
| `customStatus` | string | no | Required when Status is custom. |
| `startDate` | string | no | Beginning of created-at range, in ISO 8601 format. |
| `endDate` | string | no | End of created-at range, in ISO 8601 format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientGuid": "string",
      "createdAt": "string",
      "departmentId": 1,
      "deviceGuid": "string",
      "formId": 1,
      "id": 1,
      "revisedAt": "string",
      "revision": true,
      "status": "string",
      "submissionName": "Ava Chen",
      "submissionNumber": "string",
      "type": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientGuid` | string |  |
| `createdAt` | string |  |
| `departmentId` | number |  |
| `deviceGuid` | string |  |
| `formId` | number |  |
| `id` | number |  |
| `revisedAt` | string |  |
| `revision` | boolean |  |
| `status` | string |  |
| `submissionName` | string |  |
| `submissionNumber` | string |  |
| `type` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native GoCanvas API, this operation is `GET /submissions` (base URL `https://www.gocanvas.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-submissions.md) for the provider-specific parameters and requirements.

