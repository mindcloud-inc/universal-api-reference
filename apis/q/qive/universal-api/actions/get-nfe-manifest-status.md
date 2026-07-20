# Qive: Get NFe Manifest Status



```
GET https://connect.mindcloud.co/v1/universal/qive/latest/actions/get-nfe-manifest-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qive/latest/actions/get-nfe-manifest-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qive/latest/actions/get-nfe-manifest-status?${params}`, {
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
| `accessKeys` | string | no | NFe access keys to check manifest status for. |
| `requestIds` | string | no | Manifest request IDs to check status for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "access_key": "string",
      "code": 1,
      "status": {
        "code": 1,
        "message": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access_key` | string |  |
| `code` | number |  |
| `status.code` | number |  |
| `status.message` | string |  |

## Native endpoint

Through the native Qive API, this operation is `GET /v1/nfe/manifest/status` (base URL `https://sandbox-api.arquivei.com.br`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-nfe-manifest-status.md) for the provider-specific parameters and requirements.

