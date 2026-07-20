# Systeme.io: Remove Contact Tag

Removes a tag from a contact in Systeme.io.

```
DELETE https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/remove-contact-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Systeme.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/remove-contact-tag?connectionId=$CONNECTION_ID&id=string&tagId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "tagId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/remove-contact-tag?${params}`, {
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
| `id` | string | yes | Contact identifier. |
| `tagId` | string | yes | Tag identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "tagId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `tagId` | string |  |

## Native endpoint

Through the native Systeme.io API, this operation is `DELETE /api/contacts/:id/tags/:tagId` (base URL `https://api.systeme.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-contact-tag.md) for the provider-specific parameters and requirements.

