# jo4.io: Add A/B Test Variant



```
POST https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/add-variant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a jo4.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/add-variant" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "destinationUrl": "https://example.com",
  "name": "Ava Chen",
  "percentage": 1,
  "slug": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/add-variant', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "destinationUrl": "https://example.com",
    "name": "Ava Chen",
    "percentage": 1,
    "slug": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `destinationUrl` | string | yes |  |
| `name` | string | yes |  |
| `percentage` | number | yes |  |
| `slug` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conversionCount": 1,
      "conversionRate": 1,
      "createdTime": 1,
      "destinationUrl": "https://example.com",
      "displayOrder": 1,
      "id": 1,
      "isActive": true,
      "isControl": true,
      "isWinner": true,
      "modifiedTime": 1,
      "name": "Ava Chen",
      "percentage": 1,
      "slug": "string",
      "totalValue": 1,
      "urlId": 1,
      "visitorCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conversionCount` | number |  |
| `conversionRate` | number |  |
| `createdTime` | number |  |
| `destinationUrl` | string |  |
| `displayOrder` | number |  |
| `id` | number |  |
| `isActive` | boolean |  |
| `isControl` | boolean |  |
| `isWinner` | boolean |  |
| `modifiedTime` | number |  |
| `name` | string |  |
| `percentage` | number |  |
| `slug` | string |  |
| `totalValue` | number |  |
| `urlId` | number |  |
| `visitorCount` | number |  |

## Native endpoint

Through the native jo4.io API, this operation is `POST /protected/url/:slug/ab-test/variants` (base URL `https://jo4-api.jo4.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-variant.md) for the provider-specific parameters and requirements.

