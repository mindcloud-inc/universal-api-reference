# Clever Elements: Get Subscriber By Email



```
GET https://connect.mindcloud.co/v1/universal/cleverElements/latest/actions/get-subscriber-by-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clever Elements `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cleverElements/latest/actions/get-subscriber-by-email?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cleverElements/latest/actions/get-subscriber-by-email?${params}`, {
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
      "SOAP-ENV:Envelope": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `SOAP-ENV:Envelope` | object | Raw SOAP envelope returned by Clever Elements. |

## Native endpoint

Through the native Clever Elements API, this operation is `POST /` (base URL `http://api.sendcockpit.com/server.php`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscriber-by-email.md) for the provider-specific parameters and requirements.

