# Docmosis: Cancel Upload Template Batch



```
DELETE https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/cancel-upload-template-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docmosis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/cancel-upload-template-batch?connectionId=$CONNECTION_ID&userJobId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userJobId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/cancel-upload-template-batch?${params}`, {
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
| `userJobId` | string | yes | Identifier for the template batch upload job to cancel. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "longMsg": "string",
      "shortMsg": "string",
      "succeeded": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `longMsg` | string | Detailed status message from Docmosis. |
| `shortMsg` | string | Short status message from Docmosis. |
| `succeeded` | boolean | Whether the batch cancel request succeeded. |

## Native endpoint

Through the native Docmosis API, this operation is `POST /uploadTemplateBatchCancel` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-upload-template-batch.md) for the provider-specific parameters and requirements.

