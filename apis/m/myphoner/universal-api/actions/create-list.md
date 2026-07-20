# Myphoner: Create List

Creates a new list in Myphoner.

```
POST https://connect.mindcloud.co/v1/universal/myphoner/latest/actions/create-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Myphoner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/myphoner/latest/actions/create-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/myphoner/latest/actions/create-list', {
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
| `description` | string | no | Script or description for the list. |
| `name` | string | yes | The name of the new Myphoner list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categories": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "leadsCount": 1,
      "location": "string",
      "lockedOnDefaults": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categories` | object |  |
| `createdAt` | date |  |
| `id` | number |  |
| `leadsCount` | number |  |
| `location` | string |  |
| `lockedOnDefaults` | boolean |  |
| `name` | string |  |

## Native endpoint

Through the native Myphoner API, this operation is `POST /lists` (base URL `https://{{credentials.subdomain}}.myphoner.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-list.md) for the provider-specific parameters and requirements.

