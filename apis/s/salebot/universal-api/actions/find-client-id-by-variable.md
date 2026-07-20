# Salebot: Find Client ID by Variable



```
GET https://connect.mindcloud.co/v1/universal/salebot/latest/actions/find-client-id-by-variable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salebot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salebot/latest/actions/find-client-id-by-variable?connectionId=$CONNECTION_ID&variable=string&value=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variable": "string",
  "value": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salebot/latest/actions/find-client-id-by-variable?${params}`, {
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
| `variable` | string | yes | Variable name to search. |
| `value` | string | yes | Variable value to match. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientId": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientId` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Salebot API, this operation is `GET /find_client_id_by_var` (base URL `https://chatter.salebot.pro/api/{{credentials.apiKey}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-client-id-by-variable.md) for the provider-specific parameters and requirements.

