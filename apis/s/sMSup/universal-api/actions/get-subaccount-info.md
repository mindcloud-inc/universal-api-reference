# SMSup: Get Subaccount Info



```
GET https://connect.mindcloud.co/v1/universal/sMSup/latest/actions/get-subaccount-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMSup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSup/latest/actions/get-subaccount-info?connectionId=$CONNECTION_ID&userName=subaccount_user_name" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userName": "subaccount_user_name"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSup/latest/actions/get-subaccount-info?${params}`, {
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
| `userName` | string | yes | Username of the subaccount. Example: `subaccount_user_name`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "balance": "string",
      "currency": "string",
      "email": "ava@example.com",
      "userName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | string |  |
| `currency` | string |  |
| `email` | string |  |
| `userName` | string |  |

## Native endpoint

Through the native SMSup API, this operation is `POST /api/3.0/subaccount/get-info` (base URL `https://api.gateway360.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subaccount-info.md) for the provider-specific parameters and requirements.

