# Constant Contact: List Contact Tags

Retrieves contact tags from Constant Contact.

```
GET https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/list-contact-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Constant Contact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/list-contact-tags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/constantContact/latest/actions/list-contact-tags?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `limit` | number | no | Number of tag results per page (up to 500). Example: `50`. |
| `includeCount` | boolean | no | Include contacts_count values in each tag result. Example: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "links": {},
      "tags": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `links` | object |  |
| `tags` | array<object> |  |

## Native endpoint

Through the native Constant Contact API, this operation is `GET /contact_tags` (base URL `https://api.cc.email/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-tags.md) for the provider-specific parameters and requirements.

