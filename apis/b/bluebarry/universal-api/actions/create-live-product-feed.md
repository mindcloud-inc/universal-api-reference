# Bluebarry: Create Live Product Feed

Creates a new live product feed in Bluebarry.

```
POST https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/create-live-product-feed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bluebarry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/create-live-product-feed" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/create-live-product-feed', {
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
      "clonedFrom": "string",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "creatorId": "string",
      "id": "string",
      "lastSyncDate": "2026-05-07T12:00:00.000Z",
      "lastSyncErrorMessage": "string",
      "lastSyncStatus": "string",
      "mappingRules": [
        {}
      ],
      "modifiedDate": "2026-05-07T12:00:00.000Z",
      "modifierId": "string",
      "name": "Ava Chen",
      "productFeedIdentifierColumn": "string",
      "reference": "string",
      "tenant": "string",
      "tenantId": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clonedFrom` | string |  |
| `createdDate` | date |  |
| `creatorId` | string |  |
| `id` | string |  |
| `lastSyncDate` | date |  |
| `lastSyncErrorMessage` | string |  |
| `lastSyncStatus` | string |  |
| `mappingRules` | array<object> |  |
| `modifiedDate` | date |  |
| `modifierId` | string |  |
| `name` | string |  |
| `productFeedIdentifierColumn` | string |  |
| `reference` | string |  |
| `tenant` | string |  |
| `tenantId` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Bluebarry API, this operation is `POST /data/LiveProductFeeds` (base URL `https://data.bluebarry.ai/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-live-product-feed.md) for the provider-specific parameters and requirements.

