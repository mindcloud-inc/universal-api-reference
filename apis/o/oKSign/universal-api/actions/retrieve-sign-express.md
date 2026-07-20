# OKSign: Retrieve Sign Express

Retrieves a Sign Express request from OKSign.

```
GET https://connect.mindcloud.co/v1/universal/oKSign/latest/actions/retrieve-sign-express
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OKSign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oKSign/latest/actions/retrieve-sign-express?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oKSign/latest/actions/retrieve-sign-express?${params}`, {
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
      "reason": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `reason` | object | Retrieved Sign Express payload. |
| `status` | string |  |

## Native endpoint

Through the native OKSign API, this operation is `GET /signexpress/retrieve` (base URL `https://www.oksign.be/services/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-sign-express.md) for the provider-specific parameters and requirements.

