# turboSMTP: Get Email Validation List Summary

Retrieves an email validation list summary from turboSMTP.

```
GET https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/get-email-validation-list-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a turboSMTP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/get-email-validation-list-summary?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/get-email-validation-list-summary?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "creation_time": "string",
      "file_name": "Ava Chen",
      "id": 1,
      "is_processed": true,
      "percentage": 1,
      "status_summary": [
        {}
      ],
      "total_emails": 1,
      "total_processed": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creation_time` | string |  |
| `file_name` | string |  |
| `id` | number |  |
| `is_processed` | boolean |  |
| `percentage` | number |  |
| `status_summary` | array<object> |  |
| `total_emails` | number |  |
| `total_processed` | number |  |

## Native endpoint

Through the native turboSMTP API, this operation is `GET /emailvalidation/lists/{Id}` (base URL `https://pro.api.serversmtp.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email-validation-list-summary.md) for the provider-specific parameters and requirements.

