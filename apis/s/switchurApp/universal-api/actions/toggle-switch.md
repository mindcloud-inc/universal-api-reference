# Switchur App: Toggle Switch



```
PUT https://connect.mindcloud.co/v1/universal/switchurApp/latest/actions/toggle-switch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Switchur App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/switchurApp/latest/actions/toggle-switch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/switchurApp/latest/actions/toggle-switch', {
  method: 'PUT',
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
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Switchur response message describing the updated item state |

## Native endpoint

Through the native Switchur App API, this operation is `PUT {{credentials.webhookToggleUrl}}` (base URL `https://api.switchur.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/toggle-switch.md) for the provider-specific parameters and requirements.

