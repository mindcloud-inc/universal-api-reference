# Tricentis qTest: List Defect Comments

Retrieves defect comments from Tricentis qTest.

```
GET https://connect.mindcloud.co/v1/universal/tricentisQTest/latest/actions/list-defect-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tricentis qTest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tricentisQTest/latest/actions/list-defect-comments?connectionId=$CONNECTION_ID&projectId=1&idOrKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1",
  "idOrKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tricentisQTest/latest/actions/list-defect-comments?${params}`, {
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

Through the native Tricentis qTest API, this operation is `GET /projects/{projectId}/defects/{idOrKey}/comments` (base URL `https://mindcloudapps.qtestnet.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-defect-comments.md) for the provider-specific parameters and requirements.

