# GoCanvas: List Submission Revisions



```
GET https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/list-submission-revisions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCanvas `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/list-submission-revisions?connectionId=$CONNECTION_ID&submissionId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "submissionId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/list-submission-revisions?${params}`, {
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
| `submissionId` | number | yes | The ID of the submission. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "entryId": 1,
      "id": 1,
      "newData": "string",
      "previousData": "string",
      "revisionNumber": 1,
      "type": "string",
      "userEmail": "ava@example.com",
      "userId": 1,
      "valueId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `entryId` | number |  |
| `id` | number |  |
| `newData` | string |  |
| `previousData` | string |  |
| `revisionNumber` | number |  |
| `type` | string |  |
| `userEmail` | string |  |
| `userId` | number |  |
| `valueId` | number |  |

## Native endpoint

Through the native GoCanvas API, this operation is `GET /submissions/:submissionId/revisions` (base URL `https://www.gocanvas.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-submission-revisions.md) for the provider-specific parameters and requirements.

