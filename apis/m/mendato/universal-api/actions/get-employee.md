# Mendato: Get Employee



```
GET https://connect.mindcloud.co/v1/universal/mendato/latest/actions/get-employee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mendato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mendato/latest/actions/get-employee?connectionId=$CONNECTION_ID&variables=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mendato/latest/actions/get-employee?${params}`, {
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
| `variables` | object | yes | GraphQL variables object for the Mendato employee query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "employee": {
        "city": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "email": "ava@example.com",
        "firstName": "Ava",
        "fullPersonnelNumber": "string",
        "hasDrivingLicenceClassB": true,
        "id": "string",
        "lastName": "Chen",
        "phone": "string",
        "salutation": "string",
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `employee.city` | string |  |
| `employee.createdAt` | date |  |
| `employee.email` | string |  |
| `employee.firstName` | string |  |
| `employee.fullPersonnelNumber` | string |  |
| `employee.hasDrivingLicenceClassB` | boolean |  |
| `employee.id` | string |  |
| `employee.lastName` | string |  |
| `employee.phone` | string |  |
| `employee.salutation` | string |  |
| `employee.status` | string |  |

## Native endpoint

Through the native Mendato API, this operation is `POST /graphql` (base URL `https://api.mendato.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-employee.md) for the provider-specific parameters and requirements.

