# Navigatr: List Badges



```
GET https://connect.mindcloud.co/v1/universal/navigatr/latest/actions/list-badges
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Navigatr `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/navigatr/latest/actions/list-badges?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/navigatr/latest/actions/list-badges?${params}`, {
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
| `issuerId` | number | no |  |
| `communityId` | number | no | Community ID. Runtime verification shows this endpoint requires provider_id or community_id for this account. |
| `qaCommunityId` | number | no |  |
| `providerId` | number | no | Provider ID. Runtime verification shows this endpoint requires provider_id or community_id for this account. |
| `keyword` | string | no |  |
| `status` | string | no |  |
| `type` | string | no |  |
| `recipientType` | string | no |  |
| `source` | string | no |  |
| `featured` | boolean | no |  |
| `qaRequired` | boolean | no |  |
| `orderBy` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {
          "community_ids": [
            1
          ],
          "description": "string",
          "earn_url": "https://example.com",
          "external_url": "https://example.com",
          "featured": true,
          "id": 1,
          "image_url": "https://example.com",
          "information_url": "https://example.com",
          "issuer_id": 1,
          "issuer": {
            "id": 1,
            "name": "Ava Chen"
          },
          "name": "Ava Chen",
          "provider_ids": [
            1
          ],
          "qa_required": true,
          "recipient_type": "string",
          "source": "string",
          "status": "string",
          "time_created": "2026-05-07T12:00:00.000Z",
          "time_updated": "2026-05-07T12:00:00.000Z",
          "type": "string",
          "url": "https://example.com"
        }
      ],
      "page": 1,
      "pages": 1,
      "size": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items[].community_ids[]` | number | Community IDs |
| `items[].description` | string | Badge description |
| `items[].earn_url` | string | Badge earn URL |
| `items[].external_url` | string | Badge external URL |
| `items[].featured` | boolean | Whether the badge is featured |
| `items[].id` | number | Badge ID |
| `items[].image_url` | string | Badge image URL |
| `items[].information_url` | string | Badge information URL |
| `items[].issuer_id` | number | Issuer ID |
| `items[].issuer.id` | number | Issuer record ID |
| `items[].issuer.name` | string | Issuer name |
| `items[].name` | string | Badge name |
| `items[].provider_ids[]` | number | Provider IDs |
| `items[].qa_required` | boolean | Whether QA is required |
| `items[].recipient_type` | string | Badge recipient type |
| `items[].source` | string | Badge source |
| `items[].status` | string | Badge status |
| `items[].time_created` | date | Creation timestamp |
| `items[].time_updated` | date | Last update timestamp |
| `items[].type` | string | Badge type |
| `items[].url` | string | Public badge URL |
| `page` | number | Current page number |
| `pages` | number | Total number of pages |
| `size` | number | Page size |
| `total` | number | Total number of badges |

## Native endpoint

Through the native Navigatr API, this operation is `GET /badge/` (base URL `https://api.navigatr.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-badges.md) for the provider-specific parameters and requirements.

