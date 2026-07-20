# HR Partner: Add or Update Employee



```
PUT https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/add-or-update-employee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HR Partner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/add-or-update-employee" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/add-or-update-employee', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "customData": {},
      "email": "ava@example.com",
      "employeeAddresses": [
        {}
      ],
      "employeeContacts": [
        {}
      ],
      "firstNames": "Ava",
      "fullName": "Ava Chen",
      "isActive": true,
      "lastName": "Chen",
      "tags": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `customData` | object |  |
| `email` | string |  |
| `employeeAddresses` | array<object> |  |
| `employeeContacts` | array<object> |  |
| `firstNames` | string |  |
| `fullName` | string |  |
| `isActive` | boolean |  |
| `lastName` | string |  |
| `tags` | array<object> |  |

## Native endpoint

Through the native HR Partner API, this operation is `POST /employee` (base URL `https://api.hrpartner.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-or-update-employee.md) for the provider-specific parameters and requirements.

