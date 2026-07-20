# Mailchimp: List Member Tags

Retrieves tags for a member from a Mailchimp audience.

```
GET https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/list-member-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailchimp `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/list-member-tags?connectionId=$CONNECTION_ID&limit=25&offset=0&list_id=string&subscriber_hash=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "list_id": "string",
  "subscriber_hash": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/list-member-tags?${params}`, {
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
| `exclude_fields` | string | no |  |
| `fields` | string | no |  |
| `list_id` | string | yes | The unique ID for the Mailchimp audience. |
| `subscriber_hash` | string | yes | MD5 hash of the lowercase subscriber email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "tags": [
        [
          "string"
        ]
      ],
      "totalItems": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `tags[]` | array<string> |  |
| `totalItems` | number |  |

## Native endpoint

Through the native Mailchimp API, this operation is `GET lists/:list_id/members/:subscriber_hash/tags` (base URL `https://{{credentials.serverPrefix}}.api.mailchimp.com/3.0/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-member-tags.md) for the provider-specific parameters and requirements.

