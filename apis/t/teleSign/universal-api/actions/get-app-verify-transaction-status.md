# TeleSign: Get App Verify Transaction Status



```
GET https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/get-app-verify-transaction-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TeleSign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/get-app-verify-transaction-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teleSign/latest/actions/get-app-verify-transaction-status?${params}`, {
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
      "errors": [
        {}
      ],
      "reference_id": "string",
      "status": {
        "code": 1,
        "description": "string",
        "updated_on": "string"
      },
      "sub_resource": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<object> | Errors returned by TeleSign. |
| `reference_id` | string | Verification transaction reference ID. |
| `status.code` | number | Provider status code. |
| `status.description` | string | Provider status description. |
| `status.updated_on` | string | Timestamp when status was last updated. |
| `sub_resource` | string | TeleSign verification sub-resource. |

## Native endpoint

Through the native TeleSign API, this operation is `GET /v1/verify/auto/voice/{reference_id}` (base URL `https://rest-ww.telesign.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-app-verify-transaction-status.md) for the provider-specific parameters and requirements.

