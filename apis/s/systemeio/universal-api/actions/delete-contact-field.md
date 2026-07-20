# Systeme.io: Delete Contact Field

Deletes an existing contact field from Systeme.io.

```
DELETE https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/delete-contact-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Systeme.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/delete-contact-field?connectionId=$CONNECTION_ID&slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/systemeio/latest/actions/delete-contact-field?${params}`, {
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
| `slug` | string | yes | Contact field slug. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "slug": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `slug` | string |  |

## Native endpoint

Through the native Systeme.io API, this operation is `DELETE /api/contact_fields/:slug` (base URL `https://api.systeme.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-contact-field.md) for the provider-specific parameters and requirements.

