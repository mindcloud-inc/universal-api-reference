# Heymarket SMS: Create Contact



```
POST https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Heymarket SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "phone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "phone": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `phone` | string | yes | Contact phone number in E.164 format without the plus sign. |
| `first` | string | no | Contact first name. |
| `last` | string | no | Contact last name. |
| `displayName` | string | no | Contact display name. |
| `email` | string | no | Contact email address. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `custom` | object | no | Contact custom fields object keyed by custom field id. |
| `avatar` | string | no | Avatar image URL. |
| `assigneeId` | number | no | Team member id to assign as the contact owner. |
| `tags[]` | array<object> | no | Array of tag objects to assign to the contact. |
| `tags[].tagId` | number | no | Tag id within each tag object. |
| `isOptedOut` | boolean | no | Whether the contact is opted out of messaging. |

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

Through the native Heymarket SMS API, this operation is `POST /v1/contact` (base URL `https://api.heymarket.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

