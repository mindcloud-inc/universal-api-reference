# Tricentis qTest: Get Defect Comment

Retrieves a defect comment from Tricentis qTest.

```
GET https://connect.mindcloud.co/v1/universal/tricentisQTest/latest/actions/get-defect-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tricentis qTest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tricentisQTest/latest/actions/get-defect-comment?connectionId=$CONNECTION_ID&projectId=1&idOrKey=string&commentId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1",
  "idOrKey": "string",
  "commentId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tricentisQTest/latest/actions/get-defect-comment?${params}`, {
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
| `projectId` | number | yes | ID of the qTest project. |
| `idOrKey` | string | yes | PID or ID of the Defect. |
| `commentId` | number | yes | ID of the comment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": {},
      "body": "string",
      "created_date": "2026-05-07T12:00:00.000Z",
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | object |  |
| `body` | string |  |
| `created_date` | date |  |
| `id` | number |  |

## Native endpoint

Through the native Tricentis qTest API, this operation is `GET /projects/{projectId}/defects/{idOrKey}/comments/{commentId}` (base URL `https://mindcloudapps.qtestnet.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-defect-comment.md) for the provider-specific parameters and requirements.

