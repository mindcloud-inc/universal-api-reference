# Lead Identity Check: Authenticate Connection



```
GET https://connect.mindcloud.co/v1/universal/leadIdentityCheck/latest/actions/authenticate-connection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lead Identity Check `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadIdentityCheck/latest/actions/authenticate-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadIdentityCheck/latest/actions/authenticate-connection?${params}`, {
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
      "email": "ava@example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Account email associated with the supplied API key. |

## Native endpoint

Through the native Lead Identity Check API, this operation is `POST /zapier/authentication` (base URL `https://leadidentitycheck-node.vercel.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/authenticate-connection.md) for the provider-specific parameters and requirements.

