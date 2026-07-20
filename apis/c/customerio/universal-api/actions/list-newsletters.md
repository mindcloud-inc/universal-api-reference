# Customer.io: List Newsletters

Retrieves newsletters from Customer.io.

```
GET https://connect.mindcloud.co/v1/universal/customerio/latest/actions/list-newsletters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Customer.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customerio/latest/actions/list-newsletters?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customerio/latest/actions/list-newsletters?${params}`, {
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
| `sort` | list<string> | no | Sort newsletters in chronological asc or reverse chronological desc order. One of: `asc`, `desc`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentIds": [
        1
      ],
      "created": 1,
      "deduplicateId": "string",
      "id": 1,
      "name": "Ava Chen",
      "recipientSegmentIds": [
        1
      ],
      "sentAt": 1,
      "subscriptionTopicId": 1,
      "tags": [
        "string"
      ],
      "type": "string",
      "updated": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentIds` | array<number> | The content IDs included in the newsletter. |
| `created` | number | Unix timestamp when the newsletter was created. |
| `deduplicateId` | string | The deduplication token for the newsletter. |
| `id` | number | The identifier for the newsletter. |
| `name` | string | The name of the newsletter. |
| `recipientSegmentIds` | array<number> | Segments used to filter newsletter recipients. |
| `sentAt` | number | Unix timestamp when the newsletter was last sent. |
| `subscriptionTopicId` | number | The subscription topic ID for the newsletter. |
| `tags` | array<string> | Tags applied to the newsletter. |
| `type` | string | The newsletter delivery type. |
| `updated` | number | Unix timestamp when the newsletter was last updated. |

## Native endpoint

Through the native Customer.io API, this operation is `GET /v1/newsletters` (base URL `https://api.customer.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-newsletters.md) for the provider-specific parameters and requirements.

