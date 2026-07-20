# jo4.io: List A/B Test Variants



```
GET https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/get-variants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a jo4.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/get-variants?connectionId=$CONNECTION_ID&slug=de80effb9e48402a83afc77f947f82e4" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slug": "de80effb9e48402a83afc77f947f82e4"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/get-variants?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `slug` | string | yes | Default: `de80effb9e48402a83afc77f947f82e4`. |

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

Through the native jo4.io API, this operation is `GET /protected/url/:slug/ab-test/variants` (base URL `https://jo4-api.jo4.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-variants.md) for the provider-specific parameters and requirements.

