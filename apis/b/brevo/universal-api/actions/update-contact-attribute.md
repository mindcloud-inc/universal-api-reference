# Brevo: Update Contact Attribute



```
PUT https://connect.mindcloud.co/v1/universal/brevo/latest/actions/update-contact-attribute
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brevo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/brevo/latest/actions/update-contact-attribute" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "attributeCategory": "string",
  "attributeName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/brevo/latest/actions/update-contact-attribute', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "attributeCategory": "string",
    "attributeName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `attributeCategory` | string | yes | Attribute category, for example normal or transactional. |
| `attributeName` | string | yes | Attribute name to update. |
| `multiCategoryOptions` | object<string> | no | Array of string options when updating a multi-category attribute. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | The raw response body. |

## Native endpoint

Through the native Brevo API, this operation is `PUT /v3/contacts/attributes/:attributeCategory/:attributeName` (base URL `https://api.brevo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact-attribute.md) for the provider-specific parameters and requirements.

