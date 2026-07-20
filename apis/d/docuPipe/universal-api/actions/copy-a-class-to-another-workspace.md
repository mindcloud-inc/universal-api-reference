# DocuPipe: Copy a Class to Another Workspace

Copies a class to another DocuPipe workspace.

```
POST https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/copy-a-class-to-another-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPipe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/copy-a-class-to-another-workspace" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "classId": "string",
  "targetWorkspaceApiKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/copy-a-class-to-another-workspace', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "classId": "string",
    "targetWorkspaceApiKey": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `classId` | string | yes | Unique identifier of the class to copy. |
| `targetWorkspaceApiKey` | string | yes | API key of the target workspace. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "classId": "string",
      "className": "Ava Chen",
      "description": "string",
      "timestamp": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `classId` | string | Unique identifier of the classification object. |
| `className` | string | Name of the class. |
| `description` | string | Description of the class. |
| `timestamp` | string | Timestamp of the classification creation. |

## Native endpoint

Through the native DocuPipe API, this operation is `POST /copy/classification` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/copy-a-class-to-another-workspace.md) for the provider-specific parameters and requirements.

