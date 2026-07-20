# Verificaremails: Create Email Batch Validation

Creates an email batch validation in Verificaremails.

```
POST https://connect.mindcloud.co/v1/universal/verificaremails/latest/actions/create-email-batch-validation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Verificaremails `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/verificaremails/latest/actions/create-email-batch-validation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "column": "A"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/verificaremails/latest/actions/create-email-batch-validation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string",
    "column": "A"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | CSV, XLS, XLSX, or TXT file containing the email values to validate. |
| `column` | string | yes | Column letter or number containing the email values. Example: `A`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sendEmail` | list | no | Send a completion email when processing finishes. One of: `No`, `Yes`. Default: `0`. |
| `callbackUrl` | string | no | Webhook URL to call after the batch completes. Example: `https://example.com/webhooks/verificaremails`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "requestId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `requestId` | string | Provider-issued batch request ID for checking validation status later. |

## Native endpoint

Through the native Verificaremails API, this operation is `POST /email/validate/multiple` (base URL `https://dashboard.verificaremails.com/myapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-email-batch-validation.md) for the provider-specific parameters and requirements.

