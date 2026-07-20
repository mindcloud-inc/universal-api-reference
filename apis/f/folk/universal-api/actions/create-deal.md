# folk: Create Deal

Creates a new deal in folk.

```
POST https://connect.mindcloud.co/v1/universal/folk/latest/actions/create-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a folk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/folk/latest/actions/create-deal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": "string",
  "objectType": "Deals",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/folk/latest/actions/create-deal', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": "string",
    "objectType": "Deals",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupId` | string | yes | The group ID that owns the deal object field. |
| `objectType` | string | yes | The exact deal object type name from group custom fields, such as Deals. Default: `Deals`. |
| `name` | string | yes | The display name of the deal. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companies": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {},
      "customFieldValues": {},
      "id": "string",
      "name": "Ava Chen",
      "people": [
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
| `companies` | array<object> |  |
| `createdAt` | date |  |
| `createdBy` | object |  |
| `customFieldValues` | object |  |
| `id` | string |  |
| `name` | string |  |
| `people` | array<object> |  |

## Native endpoint

Through the native folk API, this operation is `POST /v1/groups/:groupId/:objectType` (base URL `https://api.folk.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-deal.md) for the provider-specific parameters and requirements.

