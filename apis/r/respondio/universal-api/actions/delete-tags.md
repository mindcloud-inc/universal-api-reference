# respond.io: Delete Tags

Deletes tags from a contact in respond.io.

```
DELETE https://connect.mindcloud.co/v1/universal/respondio/latest/actions/delete-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a respond.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/respondio/latest/actions/delete-tags?connectionId=$CONNECTION_ID&identifier=string&tags=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "string",
  "tags": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/respondio/latest/actions/delete-tags?${params}`, {
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
| `identifier` | string | yes | Contact identifier (id:, email:, or phone:). |
| `identify` | string | no | Tag identifier to delete. |
| `tags` | string | yes | Tag(s) to remove. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactId` | number |  |

## Native endpoint

Through the native respond.io API, this operation is `DELETE /contact/:identifier/tag` (base URL `https://api.respond.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-tags.md) for the provider-specific parameters and requirements.

