# Flokzu: Echo



```
GET https://connect.mindcloud.co/v1/universal/flokzu/latest/actions/echo
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flokzu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flokzu/latest/actions/echo?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flokzu/latest/actions/echo?${params}`, {
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
      "param_string": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `param_string` | string | Echoed string value returned by the JSON Echo endpoint when param_string is provided. |

## Native endpoint

Through the native Flokzu API, this operation is `POST /commons/JSON/echo` (base URL `https://app.flokzu.com/flokzuopenapi/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/echo.md) for the provider-specific parameters and requirements.

