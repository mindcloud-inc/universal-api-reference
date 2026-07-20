# Salesmate: Update Contact



```
PUT https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesmate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": 1,
  "lastName": "Chen",
  "owner": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": 1,
    "lastName": "Chen",
    "owner": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | number | yes | Salesmate contact ID. |
| `firstName` | string | no | Contact first name. |
| `lastName` | string | yes | Contact last name. |
| `email` | string | no | Primary email address. |
| `mobile` | string | no | Mobile phone number. |
| `owner` | number | yes | Salesmate user ID that owns the contact. |
| `company` | number | no | Existing company ID linked to the contact. |
| `designation` | string | no | Job title or role. |
| `website` | string | no | Website URL. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Internal description for the contact. |
| `tags` | string | no | Comma-separated tag list. |

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

Through the native Salesmate API, this operation is `PUT /contact/v4/:contactId` (base URL `https://apis.salesmate.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

