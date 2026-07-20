# HeyPoplar: List Campaign Mailings

Retrieves mailings for a HeyPoplar campaign.

```
GET https://connect.mindcloud.co/v1/universal/heyPoplar/latest/actions/list-campaign-mailings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HeyPoplar `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/heyPoplar/latest/actions/list-campaign-mailings?connectionId=$CONNECTION_ID&limit=25&offset=0&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/heyPoplar/latest/actions/list-campaign-mailings?${params}`, {
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
| `campaignId` | string | yes | ID of the campaign whose mailings should be returned. |
| `startDate` | string | no | Return only mailings created after this ISO8601 timestamp. |
| `endDate` | string | no | Return only mailings created before this ISO8601 timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "back_url": "https://example.com",
      "campaign_id": "string",
      "created_at": "string",
      "creative_id": "string",
      "front_url": "https://example.com",
      "id": "string",
      "merge_tags": {},
      "pdf_url": "https://example.com",
      "state": "string",
      "total_cost": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object | Recipient address object from the official Poplar campaign mailings response example. |
| `back_url` | string | Public URL to the back preview image from the official Poplar campaign mailings response example. |
| `campaign_id` | string | Campaign identifier from the official Poplar campaign mailings response example. |
| `created_at` | string | ISO 8601 created-at timestamp from the official Poplar campaign mailings response example. |
| `creative_id` | string | Creative identifier from the official Poplar campaign mailings response example. |
| `front_url` | string | Public URL to the front preview image from the official Poplar campaign mailings response example. |
| `id` | string | Mailer identifier from the official Poplar campaign mailings response example. |
| `merge_tags` | object | Merge tag object from the official Poplar campaign mailings response example. |
| `pdf_url` | string | Public URL to the PDF preview from the official Poplar campaign mailings response example. |
| `state` | string | Mailing state from the official Poplar campaign mailings response example. |
| `total_cost` | string | Total cost string from the official Poplar campaign mailings response example. |

## Native endpoint

Through the native HeyPoplar API, this operation is `GET /campaign/:id/mailings` (base URL `https://api.heypoplar.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-campaign-mailings.md) for the provider-specific parameters and requirements.

