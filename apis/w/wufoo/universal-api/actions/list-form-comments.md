# Wufoo: List Form Comments

Retrieves comments from a specific Wufoo form.

```
GET https://connect.mindcloud.co/v1/universal/wufoo/latest/actions/list-form-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wufoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wufoo/latest/actions/list-form-comments?connectionId=$CONNECTION_ID&identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wufoo/latest/actions/list-form-comments?${params}`, {
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
| `identifier` | string | yes | The form hash or identifier whose comments to list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commentedBy": "string",
      "commentId": 1,
      "dateCreated": "string",
      "entryId": 1,
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commentedBy` | string | Who created the comment. |
| `commentId` | number | The comment identifier. |
| `dateCreated` | string | When the comment was created. |
| `entryId` | number | The entry the comment belongs to. |
| `text` | string | The comment text. |

## Native endpoint

Through the native Wufoo API, this operation is `GET /forms/:identifier/comments.json` (base URL `https://{{credentials.subdomain}}.wufoo.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-form-comments.md) for the provider-specific parameters and requirements.

