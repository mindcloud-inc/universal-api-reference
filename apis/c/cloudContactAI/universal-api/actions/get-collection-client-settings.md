# CloudContactAI: Get Collection Client Settings



```
GET https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/get-collection-client-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CloudContactAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/get-collection-client-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudContactAI/latest/actions/get-collection-client-settings?${params}`, {
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

Through the native CloudContactAI API, this operation is `GET api/v2/collection/client/settings` (base URL `https://core.cloudcontactai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-collection-client-settings.md) for the provider-specific parameters and requirements.

