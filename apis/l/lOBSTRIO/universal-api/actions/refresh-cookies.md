# LOBSTR.IO: Refresh Cookies

Refreshes account cookies in LOBSTR.IO.

```
PUT https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/refresh-cookies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LOBSTR.IO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/refresh-cookies" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "account": "string",
  "cookies": {},
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lOBSTRIO/latest/actions/refresh-cookies', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "account": "string",
    "cookies": {},
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `account` | string | yes | The existing account identifier to refresh. |
| `cookies` | object | yes | Updated cookie values for the existing account. |
| `type` | string | yes | The account type identifier for the refreshed cookies. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "object": "string",
      "statusCode": 1,
      "statusText": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `object` | string |  |
| `statusCode` | number |  |
| `statusText` | string |  |

## Native endpoint

Through the native LOBSTR.IO API, this operation is `POST /v1/accounts/cookies` (base URL `https://api.lobstr.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/refresh-cookies.md) for the provider-specific parameters and requirements.

