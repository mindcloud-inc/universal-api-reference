# Navigatr: List Badge Assertions



```
GET https://connect.mindcloud.co/v1/universal/navigatr/latest/actions/list-badge-assertions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Navigatr `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/navigatr/latest/actions/list-badge-assertions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/navigatr/latest/actions/list-badge-assertions?${params}`, {
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
| `recipientId` | number | no | Retrieve assertions issued to a specific user. Use `0` for the current user, or `19524` for the known Navigatr test user when a concrete ID is needed. Default: `0`. |
| `badgeId` | number | no | Retrieve assertions for a specific badge. |
| `providerId` | number | no | Retrieve assertions issued by a specific provider. |
| `orderBy` | string | no | Order results by newest first by default, or by badge name / time created using the provider-supported values. |
| `keyword` | string | no | Filter badge assertions by badge names similar to the provided text. |
| `status` | string | no | Filter by one or more badge assertion statuses as a comma-separated string, such as `Pending,Claimed`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recipientEmail` | string | no | Retrieve assertions issued to a specific email address. The docs note this filter is typically admin-only. |

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
          "image_url": "https://example.com",
          "image_url_2x": "https://example.com",
          "image_url_original": "https://example.com",
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
          "recipient_organisation": "string",
          "recipient": {
            "firstname": "Ava",
            "id": 1,
            "lastname": "Chen"
          },
          "reminder_emails_sent": 1,
          "revocation_reason": "string",
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
| `items` | array<object> | Paginated badge assertion results. |
| `items[].badge_id` | number |  |
| `items[].badge_issuer_id` | number |  |
| `items[].badge.id` | number |  |
| `items[].badge.name` | string |  |
| `items[].end_date` | date |  |
| `items[].id` | number |  |
| `items[].image_url` | string |  |
| `items[].image_url_2x` | string |  |
| `items[].image_url_original` | string |  |
| `items[].issue_date` | date |  |
| `items[].issuing_method` | string |  |
| `items[].provider_id` | number |  |
| `items[].provider.id` | number |  |
| `items[].provider.name` | string |  |
| `items[].recipient_email` | string |  |
| `items[].recipient_firstname` | string |  |
| `items[].recipient_id` | number |  |
| `items[].recipient_lastname` | string |  |
| `items[].recipient_organisation` | string |  |
| `items[].recipient.firstname` | string |  |
| `items[].recipient.id` | number |  |
| `items[].recipient.lastname` | string |  |
| `items[].reminder_emails_sent` | number |  |
| `items[].revocation_reason` | string |  |
| `items[].source` | string |  |
| `items[].status` | string |  |
| `items[].time_claimed` | date |  |
| `items[].time_created` | date |  |
| `items[].time_updated` | date |  |
| `items[].time_verified` | date |  |
| `items[].url` | string |  |
| `page` | number |  |
| `pages` | number |  |
| `size` | number |  |
| `total` | number |  |

## Native endpoint

Through the native Navigatr API, this operation is `GET /badge_assertion/` (base URL `https://api.navigatr.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-badge-assertions.md) for the provider-specific parameters and requirements.

