# GREEN-API for WhatsApp: Get Instance State

Retrieves the WhatsApp instance state from GREEN-API.

```
GET https://connect.mindcloud.co/v1/universal/gREENAPIForWhatsApp/latest/actions/get-instance-state
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GREEN-API for WhatsApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gREENAPIForWhatsApp/latest/actions/get-instance-state?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gREENAPIForWhatsApp/latest/actions/get-instance-state?${params}`, {
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
      "stateInstance": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `stateInstance` | string | Instance state returned by GREEN-API. |

## Native endpoint

Through the native GREEN-API for WhatsApp API, this operation is `GET getStateInstance/:apiTokenInstance` (base URL `{{credentials.apiUrl}}/waInstance{{credentials.idInstance}}/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-instance-state.md) for the provider-specific parameters and requirements.

