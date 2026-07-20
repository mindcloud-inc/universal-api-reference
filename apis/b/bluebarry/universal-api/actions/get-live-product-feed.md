# Bluebarry: Get Live Product Feed

Retrieves a live product feed from Bluebarry.

```
GET https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/get-live-product-feed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bluebarry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/get-live-product-feed?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bluebarry/latest/actions/get-live-product-feed?${params}`, {
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
| `id` | string | yes |  |

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

Through the native Bluebarry API, this operation is `GET /data/LiveProductFeeds({id})` (base URL `https://data.bluebarry.ai/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-live-product-feed.md) for the provider-specific parameters and requirements.

