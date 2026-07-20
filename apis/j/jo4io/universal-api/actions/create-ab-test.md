# jo4.io: Create A/B Test



```
POST https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/create-ab-test
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a jo4.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/create-ab-test" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "slug": "string",
  "splitPercentage": 1,
  "variantDestination": "string",
  "variantName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/create-ab-test', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "slug": "string",
    "splitPercentage": 1,
    "variantDestination": "string",
    "variantName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `slug` | string | yes |  |
| `splitPercentage` | number | yes |  |
| `variantDestination` | string | yes |  |
| `variantName` | string | yes |  |

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

Through the native jo4.io API, this operation is `POST /protected/url/:slug/ab-test` (base URL `https://jo4-api.jo4.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ab-test.md) for the provider-specific parameters and requirements.

