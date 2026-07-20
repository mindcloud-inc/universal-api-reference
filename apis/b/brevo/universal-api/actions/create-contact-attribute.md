# Brevo: Create Contact Attribute



```
POST https://connect.mindcloud.co/v1/universal/brevo/latest/actions/create-contact-attribute
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Brevo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/brevo/latest/actions/create-contact-attribute" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "attributeCategory": "string",
  "attributeName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/brevo/latest/actions/create-contact-attribute', {
  method: 'POST',
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
| `attributeCategory` | string | yes | Attribute category such as normal, transactional, category, calculated, or global. |
| `attributeName` | string | yes | Attribute name to create. |
| `enumeration` | object | no | Array of options for category attributes. |
| `isRecurring` | boolean | no | Whether calculated values should be recurring. |
| `multiCategoryOptions` | object | no | Array of options for multiple-choice attributes. |
| `type` | string | no | Data type for normal/transactional attributes, e.g. text or multiple-choice. |
| `value` | string | no | Default/calculated value expression for calculated or global attributes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | object | The raw response body. The saved successful response was an empty object. |

## Native endpoint

Through the native Brevo API, this operation is `POST /v3/contacts/attributes/:attributeCategory/:attributeName` (base URL `https://api.brevo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact-attribute.md) for the provider-specific parameters and requirements.

