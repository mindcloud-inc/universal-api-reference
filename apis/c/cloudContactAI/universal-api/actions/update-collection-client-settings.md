# CloudContactAI: Update Collection Client Settings



```
PUT https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/update-collection-client-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CloudContactAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/update-collection-client-settings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/update-collection-client-settings', {
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
      "allowPartialPayment": true,
      "authId": "string",
      "authSecret": "string",
      "defaultCurrency": "string",
      "defaultMessage": "string",
      "gateway": "string",
      "testMode": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowPartialPayment` | boolean |  |
| `authId` | string |  |
| `authSecret` | string |  |
| `defaultCurrency` | string |  |
| `defaultMessage` | string |  |
| `gateway` | string |  |
| `testMode` | boolean |  |

## Native endpoint

Through the native CloudContactAI API, this operation is `POST api/v2/collection/client/settings` (base URL `https://core.cloudcontactai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-collection-client-settings.md) for the provider-specific parameters and requirements.

