# GoCanvas: Retrieve Submission



```
GET https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/retrieve-submission
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCanvas `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/retrieve-submission?connectionId=$CONNECTION_ID&submissionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "submissionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/retrieve-submission?${params}`, {
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
| `submissionId` | string | yes | Numeric submission ID or submission GUID. |

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

Through the native GoCanvas API, this operation is `GET /submissions/:submissionId` (base URL `https://www.gocanvas.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-submission.md) for the provider-specific parameters and requirements.

