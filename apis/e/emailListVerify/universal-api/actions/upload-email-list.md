# EmailListVerify: Upload Email List

Uploads an email list for verification in EmailListVerify.

```
POST https://connect.mindcloud.co/v1/universal/emailListVerify/latest/actions/upload-email-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EmailListVerify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/emailListVerify/latest/actions/upload-email-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileContents": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/emailListVerify/latest/actions/upload-email-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileContents": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileContents` | file | yes | CSV, TXT, or XLSX file containing one email address per row. |
| `quality` | string | no | Bulk verification quality. Standard costs 1 credit per email; high costs 2 credits per email. One of: `0`, `1`. Default: `standard`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Uploaded email list ID. |

## Native endpoint

Through the native EmailListVerify API, this operation is `POST /api/verifyApiFile` (base URL `https://api.emaillistverify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-email-list.md) for the provider-specific parameters and requirements.

