# Fliqr AI: Remove Tag From Contact

Deletes a tag assignment from a contact in Fliqr AI.

```
DELETE https://connect.mindcloud.co/v1/universal/fliqrAI/latest/actions/remove-tag-from-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fliqr AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/fliqrAI/latest/actions/remove-tag-from-contact?connectionId=$CONNECTION_ID&userId=1&tagId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "1",
  "tagId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fliqrAI/latest/actions/remove-tag-from-contact?${params}`, {
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
| `userId` | number | yes | Fliqr contact user ID. |
| `tagId` | number | yes | Tag ID to remove. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Fliqr AI API, this operation is `DELETE /users/:user_id/tags/:tag_id` (base URL `https://app.fliqr.ai/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-tag-from-contact.md) for the provider-specific parameters and requirements.

