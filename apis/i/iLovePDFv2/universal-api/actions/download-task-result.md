# iLovePDFv2: Download Task Result

Downloads output files for an iLovePDFv2 task.

```
GET https://connect.mindcloud.co/v1/universal/iLovePDFv2/latest/actions/download-task-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iLovePDFv2 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iLovePDFv2/latest/actions/download-task-result?connectionId=$CONNECTION_ID&server=string&task=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "server": "string",
  "task": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iLovePDFv2/latest/actions/download-task-result?${params}`, {
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
| `server` | string | yes | Processing server from Start Task. |
| `task` | string | yes | Task ID to download. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "file": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `file` | string |  |

## Native endpoint

Through the native iLovePDFv2 API, this operation is `GET https://:server/v1/download/:task` (base URL `https://api.ilovepdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-task-result.md) for the provider-specific parameters and requirements.

