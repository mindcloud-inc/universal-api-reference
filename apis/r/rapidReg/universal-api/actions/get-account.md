# RapidReg: Get Account

Retrieves account details from RapidReg.

```
GET https://connect.mindcloud.co/v1/universal/rapidReg/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RapidReg `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rapidReg/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rapidReg/latest/actions/get-account?${params}`, {
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
      "account": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | object | Account details object. |
| `success` | boolean | Whether the request was successful. |

## Native endpoint

Through the native RapidReg API, this operation is `POST /api/v1/get/account` (base URL `https://rapidreg.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

