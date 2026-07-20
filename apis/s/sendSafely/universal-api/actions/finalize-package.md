# SendSafely: Finalize Package



```
PUT https://connect.mindcloud.co/v1/universal/sendSafely/latest/actions/finalize-package
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendSafely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sendSafely/latest/actions/finalize-package" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendSafely/latest/actions/finalize-package', {
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
      "approvers": [
        "string"
      ],
      "message": "string",
      "needsLink": true,
      "recipients": [
        "string"
      ],
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approvers` | array<string> |  |
| `message` | string |  |
| `needsLink` | boolean |  |
| `recipients` | array<string> |  |
| `response` | string |  |

## Native endpoint

Through the native SendSafely API, this operation is `POST /package/:packageId/finalize/` (base URL `https://app.sendsafely.com/api/v2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/finalize-package.md) for the provider-specific parameters and requirements.

