# HR Partner: Get Employee



```
GET https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/get-employee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HR Partner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/get-employee?connectionId=$CONNECTION_ID&employeeCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "employeeCode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hRPartner/latest/actions/get-employee?${params}`, {
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
| `employeeCode` | string | yes | Employee code from HR Partner. |

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
      "id": 1,
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
| `id` | number |  |
| `isActive` | boolean |  |
| `lastName` | string |  |
| `tags` | array<object> |  |

## Native endpoint

Through the native HR Partner API, this operation is `GET /employee/:employeeCode` (base URL `https://api.hrpartner.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-employee.md) for the provider-specific parameters and requirements.

