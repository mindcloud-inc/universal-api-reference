# zipBoard: Get Feedback

Retrieves feedback comments from zipBoard.

```
GET https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/get-feedback
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a zipBoard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/get-feedback?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/get-feedback?${params}`, {
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
| `fileId` | string | no | Optional file ID whose feedback should be fetched. |
| `projectId` | string | no | Optional project ID whose feedback should be fetched. |
| `projectId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commentText": "string",
      "Id": "string",
      "projectId": "string",
      "projectTitle": "string",
      "taskDescription": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commentText` | string |  |
| `Id` | string |  |
| `projectId` | string |  |
| `projectTitle` | string |  |
| `taskDescription` | string |  |
| `updatedAt` | date |  |
| `userName` | string |  |

## Native endpoint

Through the native zipBoard API, this operation is `GET /issues/comments` (base URL `https://app.zipboard.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-feedback.md) for the provider-specific parameters and requirements.

