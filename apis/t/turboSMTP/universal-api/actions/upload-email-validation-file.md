# turboSMTP: Upload Email Validation File

Uploads a file for email validation in turboSMTP.

```
POST https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/upload-email-validation-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a turboSMTP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/upload-email-validation-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/upload-email-validation-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "list_id": 1,
      "total_emails": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `list_id` | number |  |
| `total_emails` | number |  |

## Native endpoint

Through the native turboSMTP API, this operation is `POST /emailvalidation/upload` (base URL `https://pro.api.serversmtp.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-email-validation-file.md) for the provider-specific parameters and requirements.

