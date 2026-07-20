# GetResponse: Get Account Login History

Retrieves login history for your GetResponse account.

```
GET https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/get-account-login-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GetResponse `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/get-account-login-history?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/getResponse/latest/actions/get-account-login-history?${params}`, {
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
      "ip": "string",
      "isSuccessful": "string",
      "loginTime": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ip` | string |  |
| `isSuccessful` | string |  |
| `loginTime` | string |  |

## Native endpoint

Through the native GetResponse API, this operation is `GET /accounts/login-history` (base URL `https://api.getresponse.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-account-login-history.md) for the provider-specific parameters and requirements.

