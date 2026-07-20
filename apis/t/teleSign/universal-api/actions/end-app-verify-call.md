# TeleSign: End App Verify Call



```
PUT https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/end-app-verify-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TeleSign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/end-app-verify-call" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/end-app-verify-call', {
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
      "resource_uri": "string",
      "status": {
        "code": 1,
        "description": "string",
        "updated_on": "string"
      },
      "sub_resource": "string",
      "verify_code": "string"
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
| `resource_uri` | string |  |
| `status.code` | number |  |
| `status.description` | string |  |
| `status.updated_on` | string |  |
| `sub_resource` | string |  |
| `verify_code` | string |  |

## Native endpoint

Through the native TeleSign API, this operation is `POST /v1/verify/auto/voice/finalize` (base URL `https://rest-ww.telesign.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/end-app-verify-call.md) for the provider-specific parameters and requirements.

