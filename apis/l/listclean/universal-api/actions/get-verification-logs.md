# Listclean: Get Verification Logs

Retrieves email verification logs from Listclean.

```
GET https://connect.mindcloud.co/v1/universal/listclean/latest/actions/get-verification-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Listclean `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/listclean/latest/actions/get-verification-logs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/listclean/latest/actions/get-verification-logs?${params}`, {
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
      "credits_deducted": 1,
      "email": "ava@example.com",
      "entered": "string",
      "error_code": "string",
      "id": 1,
      "instance_name": "Ava Chen",
      "remarks": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits_deducted` | number | Credits deducted for the verification. |
| `email` | string | Verified email address. |
| `entered` | string | Log timestamp. |
| `error_code` | string | Provider error code. |
| `id` | number | Verification log ID. |
| `instance_name` | string | Listclean instance name. |
| `remarks` | string | Provider remarks. |
| `status` | string | Verification status. |

## Native endpoint

Through the native Listclean API, this operation is `GET /verify/email/logs` (base URL `https://api.listclean.xyz/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-verification-logs.md) for the provider-specific parameters and requirements.

