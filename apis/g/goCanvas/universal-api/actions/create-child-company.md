# GoCanvas: Create Child Company



```
POST https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/create-child-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCanvas `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/create-child-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyName": "Ava Chen",
  "email": "ava@example.com",
  "firstName": "Ava",
  "lastName": "Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/create-child-company', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyName": "Ava Chen",
    "email": "ava@example.com",
    "firstName": "Ava",
    "lastName": "Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyName` | string | yes | Name of the new child company. |
| `email` | string | yes | Email and login for the new company's administrator. |
| `firstName` | string | yes | First name of the new company's administrator. |
| `lastName` | string | yes | Last name of the new company's administrator. |
| `seatCount` | number | no | Licensed seat count; 0 means unlimited. GoCanvas defaults to 1. |
| `password` | string | no | Initial password for the administrator. |
| `phone` | string | no | Phone number of the administrator. |
| `country` | string | no | Administrator's country; also determines the company's date format. |
| `baseUrl` | string | no | Child account's Simpro URL; required for Simpro partnerships. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pendoAccountId` | string | no | Analytics correlation identifier; applies only to Simpro partnerships. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GoCanvas API returns.

## Native endpoint

Through the native GoCanvas API, this operation is `POST /companies` (base URL `https://www.gocanvas.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-child-company.md) for the provider-specific parameters and requirements.

