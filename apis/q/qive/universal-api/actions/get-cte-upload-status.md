# Qive: Get CTe Upload Status



```
GET https://connect.mindcloud.co/v1/universal/qive/latest/actions/get-cte-upload-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qive/latest/actions/get-cte-upload-status?connectionId=$CONNECTION_ID&requestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qive/latest/actions/get-cte-upload-status?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `requestId` | string | yes | Upload request ID returned by the CTe upload endpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "invoices": [
        {
          "access_key": "string",
          "status": "string"
        }
      ],
      "request": {
        "request_id": "string",
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `invoices[].access_key` | string |  |
| `invoices[].status` | string |  |
| `request.request_id` | string |  |
| `request.status` | string |  |

## Native endpoint

Through the native Qive API, this operation is `GET /v1/cte/upload/status` (base URL `https://sandbox-api.arquivei.com.br`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-cte-upload-status.md) for the provider-specific parameters and requirements.

