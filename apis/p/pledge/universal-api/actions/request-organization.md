# Pledge: Request Organization

Requests an organization in Pledge.

```
POST https://connect.mindcloud.co/v1/universal/pledge/latest/actions/request-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pledge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pledge/latest/actions/request-organization" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ngoId": "string",
  "contact.email": "ava@example.com",
  "contact.firstName": "Ava",
  "contact.lastName": "Chen",
  "email": "ava@example.com",
  "firstName": "Ava",
  "lastName": "Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pledge/latest/actions/request-organization', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ngoId": "string",
    "contact.email": "ava@example.com",
    "contact.firstName": "Ava",
    "contact.lastName": "Chen",
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
| `ngoId` | string | yes | Employer identification number for the organization request. |
| `contact.email` | string | yes | Email for the requester contact. |
| `contact.firstName` | string | yes | First name for the requester contact. |
| `contact.lastName` | string | yes | Last name for the requester contact. |
| `email` | string | yes | Email for the requester. |
| `firstName` | string | yes | First name for the requester. |
| `lastName` | string | yes | Last name for the requester. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pledge API returns.

## Native endpoint

Through the native Pledge API, this operation is `POST /organizations` (base URL `https://api.pledge.to/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/request-organization.md) for the provider-specific parameters and requirements.

