# Resend: Delete Contact

Deletes an existing contact from Resend.

```
DELETE https://connect.mindcloud.co/v1/universal/resend/latest/actions/delete-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Resend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/resend/latest/actions/delete-contact?connectionId=$CONNECTION_ID&id=e169aa45-1ecf-4183-9955-b1499d5701d3" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "e169aa45-1ecf-4183-9955-b1499d5701d3"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/resend/latest/actions/delete-contact?${params}`, {
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
| `email` | string | no | Example: `ava.thompson@example.com`. |
| `id` | string | yes | Example: `e169aa45-1ecf-4183-9955-b1499d5701d3`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact": "string",
      "deleted": true,
      "object": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact` | string | Deleted contact identifier. |
| `deleted` | boolean | Whether the contact was deleted. |
| `object` | string | Object type identifier. |

## Native endpoint

Through the native Resend API, this operation is `DELETE /contacts/:id` (base URL `https://api.resend.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-contact.md) for the provider-specific parameters and requirements.

