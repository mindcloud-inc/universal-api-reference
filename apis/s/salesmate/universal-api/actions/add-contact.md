# Salesmate: Add Contact



```
POST https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/add-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesmate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/add-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "lastName": "Chen",
  "owner": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salesmate/latest/actions/add-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
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
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |

## Native endpoint

Through the native Salesmate API, this operation is `POST /contact/v4` (base URL `https://apis.salesmate.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-contact.md) for the provider-specific parameters and requirements.

