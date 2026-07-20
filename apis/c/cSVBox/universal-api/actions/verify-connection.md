# CSVBox: Verify Connection



```
GET https://connect.mindcloud.co/v1/universal/cSVBox/latest/actions/verify-connection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CSVBox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cSVBox/latest/actions/verify-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cSVBox/latest/actions/verify-connection?${params}`, {
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
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Connected account details returned by CSVBox. |
| `message` | string | CSVBox authentication status message. |

## Native endpoint

Through the native CSVBox API, this operation is `POST /auth` (base URL `https://api.csvbox.io/1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-connection.md) for the provider-specific parameters and requirements.

