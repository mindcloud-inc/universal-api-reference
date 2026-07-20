# Brevo: Delete Contact Attribute



```
DELETE https://connect.mindcloud.co/v1/universal/brevo/latest/actions/delete-contact-attribute
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brevo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/brevo/latest/actions/delete-contact-attribute?connectionId=$CONNECTION_ID&attributeCategory=string&attributeName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "attributeCategory": "string",
  "attributeName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/brevo/latest/actions/delete-contact-attribute?${params}`, {
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
| `attributeCategory` | string | yes | The attribute category. |
| `attributeName` | string | yes | The attribute name. |

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

Through the native Brevo API, this operation is `DELETE /v3/contacts/attributes/:attributeCategory/:attributeName` (base URL `https://api.brevo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-contact-attribute.md) for the provider-specific parameters and requirements.

