# Housecall Pro: Create Customer



```
POST https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/create-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Housecall Pro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/create-customer', {
  method: 'POST',
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | no | Example: `Avery`. |
| `lastName` | string | no | Example: `Customer`. |
| `email` | string | no | Example: `apps+stage3-create@mindcloud.co`. |
| `company` | string | no | Example: `MindCloud`. |
| `notificationsEnabled` | boolean | no |  |
| `mobileNumber` | string | no | Example: `2132135308`. |
| `homeNumber` | string | no | Example: `2132135309`. |
| `workNumber` | string | no | Example: `2132135310`. |
| `tags[]` | array<string> | no | Accepts multiple values as an array. Example: `vip`. |
| `leadSource` | string | no | Example: `web`. |
| `notes` | string | no | Example: `Created during stage 3 buildout.`. |
| `addresses[]` | array<object> | no | Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": [
        {}
      ],
      "company": "string",
      "companyId": "string",
      "companyName": "Ava Chen",
      "createdAt": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "homeNumber": "string",
      "id": "string",
      "lastName": "Chen",
      "leadSource": "string",
      "mobileNumber": "string",
      "notes": "string",
      "notificationsEnabled": true,
      "tags": [
        "string"
      ],
      "updatedAt": "string",
      "workNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses` | array<object> |  |
| `company` | string |  |
| `companyId` | string |  |
| `companyName` | string |  |
| `createdAt` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `homeNumber` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `leadSource` | string |  |
| `mobileNumber` | string |  |
| `notes` | string |  |
| `notificationsEnabled` | boolean |  |
| `tags` | array<string> |  |
| `updatedAt` | string |  |
| `workNumber` | string |  |

## Native endpoint

Through the native Housecall Pro API, this operation is `POST /customers` (base URL `https://api.housecallpro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer.md) for the provider-specific parameters and requirements.

