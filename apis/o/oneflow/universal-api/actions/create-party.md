# Oneflow: Create Party

Creates a contract party in Oneflow.

```
POST https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/create-party
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Oneflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/create-party" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contractId": "string",
  "name": "Ava Chen",
  "type": "string",
  "participants[].name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneflow/latest/actions/create-party', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contractId": "string",
    "name": "Ava Chen",
    "type": "string",
    "participants[].name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contractId` | string | yes | The Oneflow contract ID. |
| `name` | string | yes | The name of the contract party. |
| `type` | string | yes | The party type, such as company. |
| `participants[].name` | string | yes | The participant name for the new party. |
| `participants[].signatory` | boolean | no | Whether the participant is a signatory. |
| `participants[].delivery_channel` | string | no | How Oneflow should deliver the contract to the participant. |
| `participants[].email` | string | no | The participant email when required by the delivery channel. |
| `participants[].phone_number` | string | no | The participant phone number when required by the delivery channel. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {},
      "_private_ownerside": {},
      "country_code": "string",
      "id": 1,
      "identification_number": "string",
      "my_party": true,
      "name": "Ava Chen",
      "participants": [
        {}
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | object |  |
| `_private_ownerside` | object |  |
| `country_code` | string |  |
| `id` | number |  |
| `identification_number` | string |  |
| `my_party` | boolean |  |
| `name` | string |  |
| `participants` | array<object> |  |
| `type` | string |  |

## Native endpoint

Through the native Oneflow API, this operation is `POST /contracts/:contractId/parties` (base URL `https://api.oneflow.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-party.md) for the provider-specific parameters and requirements.

