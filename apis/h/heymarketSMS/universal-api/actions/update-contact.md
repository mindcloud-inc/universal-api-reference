# Heymarket SMS: Update Contact



```
PUT https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Heymarket SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": 1,
  "phone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": 1,
    "phone": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | number | yes | Unique identifier of the contact. |
| `phone` | string | yes | Contact phone number in E.164 format without the plus sign. |
| `first` | string | no | First name. |
| `last` | string | no | Last name. |
| `displayName` | string | no | Display name for the contact. |
| `email` | string | no | Email address. |
| `tags[].tagId` | number | no | Tag identifier. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `custom` | object | no | Custom field values keyed by numeric custom field ID. |
| `avatar` | string | no | Avatar image URL. |
| `assigneeId` | number | no | Contact owner user ID. Use -1 to unassign. |
| `tags[]` | array<object> | no | Up to 5 contact tags. |
| `isOptedOut` | boolean | no | Whether the contact is opted out of messaging. |
| `overwrite` | boolean | no | When true, replaces existing custom fields instead of merging them. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "rev": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `rev` | number |  |

## Native endpoint

Through the native Heymarket SMS API, this operation is `PUT /v1/contact/:id` (base URL `https://api.heymarket.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

