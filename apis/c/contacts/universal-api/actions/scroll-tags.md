# Contacts+: Scroll Tags

Retrieves tags from Contacts+ using a scroll cursor.

```
GET https://connect.mindcloud.co/v1/universal/contacts/latest/actions/scroll-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Contacts+ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contacts/latest/actions/scroll-tags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contacts/latest/actions/scroll-tags?${params}`, {
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
| `size` | number | no | Maximum number of tags to return. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `scrollCursor` | string | no | Cursor for the next page of tags. Leave blank for the first page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "etag": "string",
      "tagData": {
        "name": "Ava Chen"
      },
      "tagId": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `etag` | string |  |
| `tagData.name` | string |  |
| `tagId` | string |  |
| `updated` | date |  |

## Native endpoint

Through the native Contacts+ API, this operation is `POST /api/v1/tags.scroll` (base URL `https://api.contactsplus.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/scroll-tags.md) for the provider-specific parameters and requirements.

