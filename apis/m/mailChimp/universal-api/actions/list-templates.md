# Mailchimp: List Templates

Retrieves templates from Mailchimp.

```
GET https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailchimp `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/list-templates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/list-templates?${params}`, {
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
| `before_date_created` | string | no |  |
| `category` | string | no |  |
| `content_type` | string | no |  |
| `created_by` | string | no |  |
| `exclude_fields` | string | no |  |
| `fields` | string | no |  |
| `folder_id` | string | no |  |
| `since_date_created` | string | no |  |
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
      "templates": [
        [
          {}
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
| `templates[]` | array<object> |  |
| `templates[].active` | boolean |  |
| `templates[].category` | string |  |
| `templates[].contentType` | string |  |
| `templates[].createdBy` | string |  |
| `templates[].dateCreated` | string |  |
| `templates[].dateEdited` | string |  |
| `templates[].dragAndDrop` | boolean |  |
| `templates[].editedBy` | string |  |
| `templates[].id` | number |  |
| `templates[].links[]` | array<object> |  |
| `templates[].links[].href` | string |  |
| `templates[].links[].method` | string |  |
| `templates[].links[].rel` | string |  |
| `templates[].links[].targetSchema` | string |  |
| `templates[].name` | string |  |
| `templates[].responsive` | boolean |  |
| `templates[].shareUrl` | string |  |
| `templates[].thumbnail` | string |  |
| `templates[].type` | string |  |
| `totalItems` | number |  |

## Native endpoint

Through the native Mailchimp API, this operation is `GET templates` (base URL `https://{{credentials.serverPrefix}}.api.mailchimp.com/3.0/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

