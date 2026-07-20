# PayTabs: Get Token Status



```
GET https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/get-token-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PayTabs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/get-token-status?connectionId=$CONNECTION_ID&token=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "token": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/payTabs/latest/actions/get-token-status?${params}`, {
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
| `token` | string | yes | Stored PayTabs token to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cardScheme": "string",
      "code": 1,
      "expiryMonth": "string",
      "expiryYear": "string",
      "message": "string",
      "token": "string",
      "tokenStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cardScheme` | string |  |
| `code` | number |  |
| `expiryMonth` | string |  |
| `expiryYear` | string |  |
| `message` | string |  |
| `token` | string |  |
| `tokenStatus` | string |  |

## Native endpoint

Through the native PayTabs API, this operation is `POST /payment/token` (base URL `{{credentials.apiBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-token-status.md) for the provider-specific parameters and requirements.

