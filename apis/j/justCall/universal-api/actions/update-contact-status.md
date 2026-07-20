# JustCall: Update Contact Status

Updates contact status in JustCall.

```
PUT https://connect.mindcloud.co/v1/universal/justCall/latest/actions/update-contact-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JustCall `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/justCall/latest/actions/update-contact-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/justCall/latest/actions/update-contact-status', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `addTo[]` | array<string> | no | Status lists to add the contact to. |
| `id` | number | no | The JustCall contact ID whose status should change. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "agentId": 1,
      "company": "string",
      "contactNumber": "string",
      "createdAt": "string",
      "email": "ava@example.com",
      "extension": 1,
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "lastUpdatedAt": "string",
      "name": "Ava Chen",
      "notes": [
        {}
      ],
      "otherNumbers": [
        {}
      ],
      "parentContactId": 1,
      "status": {},
      "statusUpdatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `agentId` | number |  |
| `company` | string |  |
| `contactNumber` | string |  |
| `createdAt` | string |  |
| `email` | string |  |
| `extension` | number |  |
| `firstName` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `lastUpdatedAt` | string |  |
| `name` | string |  |
| `notes` | array<object> |  |
| `otherNumbers` | array<object> |  |
| `parentContactId` | number |  |
| `status` | object |  |
| `statusUpdatedAt` | string |  |

## Native endpoint

Through the native JustCall API, this operation is `PUT /v2.1/contacts/status` (base URL `https://api.justcall.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact-status.md) for the provider-specific parameters and requirements.

