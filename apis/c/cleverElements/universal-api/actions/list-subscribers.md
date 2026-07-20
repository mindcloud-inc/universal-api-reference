# Clever Elements: List Subscribers



```
GET https://connect.mindcloud.co/v1/universal/cleverElements/latest/actions/list-subscribers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clever Elements `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cleverElements/latest/actions/list-subscribers?connectionId=$CONNECTION_ID&listId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cleverElements/latest/actions/list-subscribers?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listId` | string | yes | The Clever Elements list ID. |
| `start` | string | no | Zero-based start offset. Default: `0`. |
| `count` | string | no | Maximum number of subscribers to return. Default: `100`. |

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

Through the native Clever Elements API, this operation is `POST /` (base URL `http://api.sendcockpit.com/server.php`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subscribers.md) for the provider-specific parameters and requirements.

