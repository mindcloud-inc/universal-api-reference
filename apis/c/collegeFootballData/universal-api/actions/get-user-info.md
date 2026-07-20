# College Football Data: Get User Info

Retrieves user account details from College Football Data.

```
GET https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-user-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a College Football Data `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/collegeFootballData/latest/actions/get-user-info?${params}`, {
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
      "patronLevel": 1,
      "remainingCalls": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `patronLevel` | number |  |
| `remainingCalls` | number |  |

## Native endpoint

Through the native College Football Data API, this operation is `GET /info` (base URL `https://api.collegefootballdata.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-info.md) for the provider-specific parameters and requirements.

