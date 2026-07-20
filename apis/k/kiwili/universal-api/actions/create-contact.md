# Kiwili: Create Contact

Creates a new contact in Kiwili.

```
POST https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kiwili `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "EnterpriseId": 1,
  "FirstName": "Ava",
  "LastName": "Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "EnterpriseId": 1,
    "FirstName": "Ava",
    "LastName": "Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `Email` | string | no | The contact email address. |
| `EnterpriseId` | number | yes | The enterprise ID the contact belongs to. |
| `FirstName` | string | yes | The contact first name. |
| `LastName` | string | yes | The contact last name. |

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

Through the native Kiwili API, this operation is `POST /contact` (base URL `https://mindcloud.kiwili.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

