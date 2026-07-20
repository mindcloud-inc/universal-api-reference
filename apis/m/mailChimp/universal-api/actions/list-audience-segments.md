# Mailchimp: List Audience Segments

Retrieves segments from a Mailchimp audience.

```
GET https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/list-audience-segments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailchimp `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/list-audience-segments?connectionId=$CONNECTION_ID&limit=25&offset=0&list_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "list_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/list-audience-segments?${params}`, {
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
| `before_created_at` | string | no |  |
| `before_updated_at` | string | no |  |
| `exclude_fields` | string | no |  |
| `fields` | string | no |  |
| `include_cleaned` | boolean | no |  |
| `include_transactional` | boolean | no |  |
| `include_unsubscribed` | boolean | no |  |
| `list_id` | string | yes | The unique ID for the Mailchimp audience. |
| `since_created_at` | string | no |  |
| `since_updated_at` | string | no |  |
| `type` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "links": [
        [
          {}
        ]
      ],
      "listId": "string",
      "segments": [
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
| `links[]` | array<object> |  |
| `links[].href` | string |  |
| `links[].method` | string |  |
| `links[].rel` | string |  |
| `links[].schema` | string |  |
| `links[].targetSchema` | string |  |
| `listId` | string |  |
| `segments[]` | array<string> |  |
| `totalItems` | number |  |

## Native endpoint

Through the native Mailchimp API, this operation is `GET lists/:list_id/segments` (base URL `https://{{credentials.serverPrefix}}.api.mailchimp.com/3.0/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-audience-segments.md) for the provider-specific parameters and requirements.

