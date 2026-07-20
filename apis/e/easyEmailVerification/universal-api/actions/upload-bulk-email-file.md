# Easy Email Verification: Upload Bulk Email File

Creates a bulk verification job in Easy Email Verification.

```
POST https://connect.mindcloud.co/v1/universal/easyEmailVerification/latest/actions/upload-bulk-email-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easy Email Verification `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/easyEmailVerification/latest/actions/upload-bulk-email-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyEmailVerification/latest/actions/upload-bulk-email-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | Text or CSV file containing email addresses. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Easy Email Verification API returns.

## Native endpoint

Through the native Easy Email Verification API, this operation is `POST /bulk/upload` (base URL `https://api.easyemailverification.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-bulk-email-file.md) for the provider-specific parameters and requirements.

