# ITM Platform: List Programs



```
GET https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/list-programs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ITM Platform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/list-programs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iTMPlatform/latest/actions/list-programs?${params}`, {
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
      "accountId": 1,
      "endDate": "string",
      "id": 1,
      "languageId": 1,
      "name": "Ava Chen",
      "no": "string",
      "startDate": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `endDate` | string |  |
| `id` | number |  |
| `languageId` | number |  |
| `name` | string |  |
| `no` | string |  |
| `startDate` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native ITM Platform API, this operation is `GET /v2/programs` (base URL `https://api.itmplatform.com/{{credentials.company}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-programs.md) for the provider-specific parameters and requirements.

