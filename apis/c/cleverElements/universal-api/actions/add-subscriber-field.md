# Clever Elements: Add Subscriber Field



```
POST https://connect.mindcloud.co/v1/universal/cleverElements/latest/actions/add-subscriber-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clever Elements `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cleverElements/latest/actions/add-subscriber-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cleverElements/latest/actions/add-subscriber-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
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

Through the native Clever Elements API, this operation is `POST /` (base URL `http://api.sendcockpit.com/server.php`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-subscriber-field.md) for the provider-specific parameters and requirements.

