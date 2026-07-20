# Navigatr: List User Badges



```
GET https://connect.mindcloud.co/v1/universal/navigatr/latest/actions/list-user-badges
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Navigatr `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/navigatr/latest/actions/list-user-badges?connectionId=$CONNECTION_ID&limit=25&offset=0&userId=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "userId": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/navigatr/latest/actions/list-user-badges?${params}`, {
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
| `userId` | number | yes | Use 0 for the current user, or a specific user ID such as 19524 when needed. Default: `0`. |
| `orderBy` | string | no | Sort order for the user's badges. |
| `keyword` | string | no | Filter badges by keyword. |
| `status` | string | no | Filter badges by status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {
          "badge_id": 1,
          "badge_issuer_id": 1,
          "badge": {
            "id": 1,
            "name": "Ava Chen"
          },
          "end_date": "2026-05-07T12:00:00.000Z",
          "id": 1,
          "issue_date": "2026-05-07T12:00:00.000Z",
          "issuing_method": "string",
          "provider_id": 1,
          "provider": {
            "id": 1,
            "name": "Ava Chen"
          },
          "recipient_email": "ava@example.com",
          "recipient_firstname": "Ava",
          "recipient_id": 1,
          "recipient_lastname": "Chen",
          "recipient": {
            "firstname": "Ava",
            "id": 1,
            "lastname": "Chen"
          },
          "source": "string",
          "status": "string",
          "time_claimed": "2026-05-07T12:00:00.000Z",
          "time_created": "2026-05-07T12:00:00.000Z",
          "time_updated": "2026-05-07T12:00:00.000Z",
          "time_verified": "2026-05-07T12:00:00.000Z",
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
| `items[].badge_id` | number | Badge ID |
| `items[].badge_issuer_id` | number | Badge issuer ID |
| `items[].badge.id` | number | Badge record ID |
| `items[].badge.name` | string | Badge name |
| `items[].end_date` | date | End date |
| `items[].id` | number | Badge assertion ID |
| `items[].issue_date` | date | Issue date |
| `items[].issuing_method` | string | Issuing method |
| `items[].provider_id` | number | Provider ID |
| `items[].provider.id` | number | Provider record ID |
| `items[].provider.name` | string | Provider name |
| `items[].recipient_email` | string | Recipient email |
| `items[].recipient_firstname` | string | Recipient first name |
| `items[].recipient_id` | number | Recipient user ID |
| `items[].recipient_lastname` | string | Recipient last name |
| `items[].recipient.firstname` | string | Recipient first name from profile |
| `items[].recipient.id` | number | Recipient record ID |
| `items[].recipient.lastname` | string | Recipient last name from profile |
| `items[].source` | string | Source type |
| `items[].status` | string | Badge assertion status |
| `items[].time_claimed` | date | Claim timestamp |
| `items[].time_created` | date | Creation timestamp |
| `items[].time_updated` | date | Last update timestamp |
| `items[].time_verified` | date | Verification timestamp |
| `items[].url` | string | Public badge assertion URL |
| `page` | number | Current page number |
| `pages` | number | Total number of pages |
| `size` | number | Page size |
| `total` | number | Total number of badge assertions |

## Native endpoint

Through the native Navigatr API, this operation is `GET /user_detail/:user_id/badges` (base URL `https://api.navigatr.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-user-badges.md) for the provider-specific parameters and requirements.

