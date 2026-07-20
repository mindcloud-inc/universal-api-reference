# Plausible Analytics: Create Custom Property

Creates a custom property in a Plausible Analytics site.

```
POST https://connect.mindcloud.co/v1/universal/plausibleAnalytics/latest/actions/create-custom-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Plausible Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/plausibleAnalytics/latest/actions/create-custom-property" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/plausibleAnalytics/latest/actions/create-custom-property', {
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
      "property": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `property` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Plausible Analytics API, this operation is `PUT /api/v1/sites/custom-props` (base URL `https://plausible.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-custom-property.md) for the provider-specific parameters and requirements.

