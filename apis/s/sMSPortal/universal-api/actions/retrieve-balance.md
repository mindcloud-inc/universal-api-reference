# SMSPortal: Retrieve Balance



```
GET https://connect.mindcloud.co/v1/universal/sMSPortal/latest/actions/retrieve-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMSPortal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMSPortal/latest/actions/retrieve-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMSPortal/latest/actions/retrieve-balance?${params}`, {
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
      "balance": 1,
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | number | Current available SMS credit balance for the authenticated account. |
| `statusCode` | number | HTTP status code returned by the SMSPortal balance endpoint. |

## Native endpoint

Through the native SMSPortal API, this operation is `GET /Balance` (base URL `https://rest.smsportal.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-balance.md) for the provider-specific parameters and requirements.

