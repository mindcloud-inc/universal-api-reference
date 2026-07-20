# Fidel API: Update Program

Updates an existing program in Fidel API.

```
PUT https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/update-program
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fidel API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/update-program" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "programId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/update-program', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "programId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `programId` | string | yes |  |
| `name` | string | no | Name for the Program. Can be 4 - 50 characters long. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "active": true,
      "activeDate": "2026-05-07T12:00:00.000Z",
      "created": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "live": true,
      "name": "Ava Chen",
      "sync": true,
      "syncStats": {
        "status": "string"
      },
      "type": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `active` | boolean |  |
| `activeDate` | date |  |
| `created` | date |  |
| `id` | string |  |
| `live` | boolean |  |
| `name` | string |  |
| `sync` | boolean |  |
| `syncStats.status` | string |  |
| `type` | string |  |
| `updated` | date |  |

## Native endpoint

Through the native Fidel API API, this operation is `PATCH /programs/:programId` (base URL `https://api.fidel.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-program.md) for the provider-specific parameters and requirements.

