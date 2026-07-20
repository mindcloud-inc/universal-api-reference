# TeleSign: Report SMS Verify Completion



```
PUT https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/report-sms-verify-completion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TeleSign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/report-sms-verify-completion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/report-sms-verify-completion', {
  method: 'PUT',
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
      "errors": [
        {}
      ],
      "reference_id": "string",
      "status": {
        "code": "string",
        "description": "string",
        "updated_on": "string"
      },
      "subresource": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<object> |  |
| `reference_id` | string |  |
| `status.code` | string |  |
| `status.description` | string |  |
| `status.updated_on` | string |  |
| `subresource` | string |  |

## Native endpoint

Through the native TeleSign API, this operation is `PUT /v1/verify/completion/{reference_id}` (base URL `https://rest-ww.telesign.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/report-sms-verify-completion.md) for the provider-specific parameters and requirements.

