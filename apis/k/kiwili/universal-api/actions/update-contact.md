# Kiwili: Update Contact

Updates an existing contact in Kiwili.

```
PUT https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kiwili `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contact_id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contact_id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contact_id` | number | yes | The Kiwili contact ID to update. |
| `EnterpriseId` | number | no | The enterprise ID the contact belongs to. |
| `FirstName` | string | no | The updated contact first name. |
| `LastName` | string | no | The updated contact last name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Email": "ava@example.com",
      "EnterpriseId": 1,
      "FirstName": "Ava",
      "Id": 1,
      "IsActive": true,
      "LastName": "Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Email` | string |  |
| `EnterpriseId` | number |  |
| `FirstName` | string |  |
| `Id` | number |  |
| `IsActive` | boolean |  |
| `LastName` | string |  |

## Native endpoint

Through the native Kiwili API, this operation is `PUT /contact/:contact_id` (base URL `https://mindcloud.kiwili.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

