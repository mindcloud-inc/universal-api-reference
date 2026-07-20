# LastPass: Get Reporting Data

Retrieves reporting data from LastPass.

```
GET https://connect.mindcloud.co/v1/universal/lastPass/latest/actions/get-reporting-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LastPass `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lastPass/latest/actions/get-reporting-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lastPass/latest/actions/get-reporting-data?${params}`, {
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
      "action": "string",
      "data": "string",
      "ipAddress": "string",
      "serverSessionId": "string",
      "time": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string |  |
| `data` | string |  |
| `ipAddress` | string |  |
| `serverSessionId` | string |  |
| `time` | string |  |
| `username` | string |  |

## Native endpoint

Through the native LastPass API, this operation is `POST /enterpriseapi.php` (base URL `https://lastpass.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-reporting-data.md) for the provider-specific parameters and requirements.

