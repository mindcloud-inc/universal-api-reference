# OneSuite: Update Client Status

Updates a client's status in OneSuite.

```
PUT https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/update-client-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OneSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/update-client-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clientId": "string",
  "statusId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneSuite/latest/actions/update-client-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clientId": "string",
    "statusId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clientId` | string | yes | The ID of the client |
| `statusId` | string | yes | Priority status ID to assign |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedToId": {},
      "bgColor": "string",
      "businessId": "string",
      "companyId": "string",
      "createdAt": "string",
      "fgColor": "string",
      "id": "string",
      "peopleId": {},
      "priorityId": "string",
      "status": {
        "bgColor": "string",
        "borderColor": "string",
        "businessId": "string",
        "createdAt": "string",
        "fgColor": "string",
        "id": "string",
        "isDefault": true,
        "name": "Ava Chen",
        "slug": "string",
        "updatedAt": "string"
      },
      "statusId": "string",
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedToId` | object |  |
| `bgColor` | string |  |
| `businessId` | string |  |
| `companyId` | string |  |
| `createdAt` | string |  |
| `fgColor` | string |  |
| `id` | string |  |
| `peopleId` | object |  |
| `priorityId` | string |  |
| `status.bgColor` | string |  |
| `status.borderColor` | string |  |
| `status.businessId` | string |  |
| `status.createdAt` | string |  |
| `status.fgColor` | string |  |
| `status.id` | string |  |
| `status.isDefault` | boolean |  |
| `status.name` | string |  |
| `status.slug` | string |  |
| `status.updatedAt` | string |  |
| `statusId` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native OneSuite API, this operation is `PATCH /v1/clients/:client_id/status` (base URL `https://api.onesuite.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-client-status.md) for the provider-specific parameters and requirements.

