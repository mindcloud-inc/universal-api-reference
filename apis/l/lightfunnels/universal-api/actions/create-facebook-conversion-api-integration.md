# Lightfunnels: Create Facebook Conversion API Integration



```
POST https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/create-facebook-conversion-api-integration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lightfunnels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/create-facebook-conversion-api-integration" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/create-facebook-conversion-api-integration', {
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
      "createFacebookConversionApiIntegration": {
        "id": "string",
        "type": "string",
        "url": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createFacebookConversionApiIntegration` | object | Created integration. |
| `createFacebookConversionApiIntegration.id` | string | Integration id. |
| `createFacebookConversionApiIntegration.type` | string | Integration type. |
| `createFacebookConversionApiIntegration.url` | string | Integration url. |

## Native endpoint

Through the native Lightfunnels API, this operation is `POST /api/v2` (base URL `https://services.lightfunnels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-facebook-conversion-api-integration.md) for the provider-specific parameters and requirements.

