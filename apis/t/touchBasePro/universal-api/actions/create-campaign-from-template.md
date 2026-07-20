# TouchBasePro: Create Campaign From Template

Creates a new campaign from a template in TouchBasePro.

```
POST https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/create-campaign-from-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TouchBasePro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/create-campaign-from-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/touchBasePro/latest/actions/create-campaign-from-template', {
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
      "2c3b5169f32abe2b5bf6287235a5dc67": "string",
      "f9f55267a8d5cb5212bc626a3b33eb27": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `2c3b5169f32abe2b5bf6287235a5dc67` | string |  |
| `f9f55267a8d5cb5212bc626a3b33eb27` | string |  |

## Native endpoint

Through the native TouchBasePro API, this operation is `POST /email/campaigns/fromtemplate` (base URL `https://api.touchbasepro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-campaign-from-template.md) for the provider-specific parameters and requirements.

