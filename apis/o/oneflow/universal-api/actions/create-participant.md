# Oneflow: Create Participant

Creates a contract participant in Oneflow.

```
POST https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/create-participant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Oneflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/create-participant" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contractId": "string",
  "partyId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/create-participant', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contractId": "string",
    "partyId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contractId` | string | yes | The Oneflow contract ID. |
| `partyId` | string | yes | The Oneflow contract party ID. |
| `name` | string | yes | The participant name. |
| `signatory` | boolean | no | Whether the participant is a signatory. |
| `delivery_channel` | string | no | How Oneflow should deliver the contract to the participant. |
| `email` | string | no | The participant email when required by the delivery channel. |
| `phone_number` | string | no | The participant phone number when required by the delivery channel. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {},
      "_permissions": {},
      "_private_ownerside": {},
      "delivery_channel": "string",
      "delivery_status": "string",
      "draft_approver": true,
      "email": "ava@example.com",
      "id": 1,
      "identification_number": "string",
      "my_participant": true,
      "name": "Ava Chen",
      "organizer": true,
      "pending_approver": true,
      "phone_number": "string",
      "sign_method": "string",
      "sign_state": "string",
      "sign_state_updated_time": "string",
      "signatory": true,
      "title": "string",
      "two_step_authentication_method": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | object |  |
| `_permissions` | object |  |
| `_private_ownerside` | object |  |
| `delivery_channel` | string |  |
| `delivery_status` | string |  |
| `draft_approver` | boolean |  |
| `email` | string |  |
| `id` | number |  |
| `identification_number` | string |  |
| `my_participant` | boolean |  |
| `name` | string |  |
| `organizer` | boolean |  |
| `pending_approver` | boolean |  |
| `phone_number` | string |  |
| `sign_method` | string |  |
| `sign_state` | string |  |
| `sign_state_updated_time` | string |  |
| `signatory` | boolean |  |
| `title` | string |  |
| `two_step_authentication_method` | string |  |

## Native endpoint

Through the native Oneflow API, this operation is `POST /contracts/:contractId/parties/:partyId/participants` (base URL `https://api.oneflow.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-participant.md) for the provider-specific parameters and requirements.

