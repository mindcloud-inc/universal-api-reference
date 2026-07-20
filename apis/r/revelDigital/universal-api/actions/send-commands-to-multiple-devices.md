# Revel Digital: Send Commands to Multiple Devices



```
POST https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/send-commands-to-multiple-devices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Revel Digital `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/send-commands-to-multiple-devices" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/send-commands-to-multiple-devices', {
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
      "data": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string | Inferred empty response body returned by the provider for successful no-content command submissions. |
| `success` | boolean | Inferred wrapper success flag for successful no-content Revel device command requests. |

## Native endpoint

Through the native Revel Digital API, this operation is `POST /devices/commands` (base URL `https://api.reveldigital.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-commands-to-multiple-devices.md) for the provider-specific parameters and requirements.

