# Contacts+: Create Tag

Creates a new tag in Contacts+.

```
POST https://connect.mindcloud.co/v1/universal/contacts/latest/actions/create-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Contacts+ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/contacts/latest/actions/create-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tag": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/contacts/latest/actions/create-tag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tag": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tag` | object | yes | The tag object to create. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamId` | string | no | Create the tag in this team instead of personal tags. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "tag": {
        "created": "2026-05-07T12:00:00.000Z",
        "etag": "string",
        "tagData": {
          "name": "Ava Chen"
        },
        "tagId": "string",
        "updated": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `tag.created` | date |  |
| `tag.etag` | string |  |
| `tag.tagData.name` | string |  |
| `tag.tagId` | string |  |
| `tag.updated` | date |  |

## Native endpoint

Through the native Contacts+ API, this operation is `POST /api/v1/tags.create` (base URL `https://api.contactsplus.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tag.md) for the provider-specific parameters and requirements.

