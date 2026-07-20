# Gamalogic: Verify Batch Emails



```
POST https://connect.mindcloud.co/v1/universal/gamalogic/latest/actions/verify-batch-emails
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gamalogic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gamalogic/latest/actions/verify-batch-emails" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "gamalogicEmailidVrfy[]": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gamalogic/latest/actions/verify-batch-emails', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "gamalogicEmailidVrfy[]": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `gamalogicEmailidVrfy[]` | array<object> | yes | Email records to validate. Each item should include an emailid value. Example: `[object Object]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `speedRank` | number | no | Optional speed and accuracy setting. Defaults to 0; higher values are slower and more accurate. Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "batchId": 1,
      "error": true,
      "message": "string",
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batchId` | number | Batch ID used to check status and download results. |
| `error` | boolean | Whether the request returned an error. |
| `message` | string | Batch creation message. |
| `totalCount` | number | Total email addresses uploaded for verification. |

## Native endpoint

Through the native Gamalogic API, this operation is `POST /batchemailvrf` (base URL `https://gamalogic.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-batch-emails.md) for the provider-specific parameters and requirements.

