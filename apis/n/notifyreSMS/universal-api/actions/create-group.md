# Notifyre SMS: Create Group

Creates a new group in Notifyre.

```
POST https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/create-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notifyre SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/create-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/create-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Group name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdDateUtc": 1,
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdDateUtc` | number | UTC timestamp when the group was created. |
| `id` | string | Created group identifier. |
| `name` | string | Created group name. |

## Native endpoint

Through the native Notifyre SMS API, this operation is `POST /addressbook/groups` (base URL `https://api.notifyre.com/20220711`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-group.md) for the provider-specific parameters and requirements.

