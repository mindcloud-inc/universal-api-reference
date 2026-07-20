# Magileads: Create PRM Nurturing

Creates a new PRM nurturing in Magileads.

```
POST https://connect.mindcloud.co/v1/universal/magileads/latest/actions/create-prm-nurturing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Magileads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/magileads/latest/actions/create-prm-nurturing" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "filter": {},
  "contactListIds[]": [
    1
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/magileads/latest/actions/create-prm-nurturing', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "filter": {},
    "contactListIds[]": [1]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The nurturing name. |
| `filter` | object | yes | The nurturing filter object. |
| `contactListIds[]` | array<number> | yes | The contact list IDs to include in the nurturing. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nurturing_id": 1,
      "state": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nurturing_id` | number |  |
| `state` | boolean |  |

## Native endpoint

Through the native Magileads API, this operation is `POST /prm/nurturing` (base URL `https://app.api-magileads.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-prm-nurturing.md) for the provider-specific parameters and requirements.

