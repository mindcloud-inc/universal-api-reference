# SuperSend: List Contacts

Retrieves contacts from SuperSend.

```
GET https://connect.mindcloud.co/v1/universal/superSend/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperSend `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superSend/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superSend/latest/actions/list-contacts?${params}`, {
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
| `teamId` | string | no |  |
| `campaignId` | string | no |  |
| `limit` | number | no | Default: 50. Range: 1 to 100. |
| `offset` | number | no | Default: 0. Range: 0 to inf. |
| `search` | string | no |  |
| `interest` | string | no | Filter by contact status (interest). Comma-separated for multiple values. Values: interested, not_interested, meeting_request, meeting_booked, customer, future, follow_up. Use empty string or null to filter for contacts with no status. Accepts multiple values in one string, delimited by `,`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign_id": "string",
      "company": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "custom": {},
      "deleted": true,
      "email": "ava@example.com",
      "finished": true,
      "first_name": "Ava",
      "id": "string",
      "interest": "string",
      "last_name": "Chen",
      "linkedin_url": "https://example.com",
      "phone": "string",
      "team_id": "string",
      "title": "string",
      "twitter": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign_id` | string |  |
| `company` | string |  |
| `created_at` | date |  |
| `custom` | object |  |
| `deleted` | boolean |  |
| `email` | string |  |
| `finished` | boolean |  |
| `first_name` | string |  |
| `id` | string |  |
| `interest` | string |  |
| `last_name` | string |  |
| `linkedin_url` | string |  |
| `phone` | string |  |
| `team_id` | string |  |
| `title` | string |  |
| `twitter` | string |  |
| `updated_at` | date |  |
| `website` | string |  |

## Native endpoint

Through the native SuperSend API, this operation is `GET /contacts` (base URL `https://api.supersend.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

