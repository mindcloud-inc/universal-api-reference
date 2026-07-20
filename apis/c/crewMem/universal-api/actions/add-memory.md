# CrewMem: Add Memory



```
POST https://connect.mindcloud.co/v1/universal/crewMem/latest/actions/add-memory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CrewMem `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/crewMem/latest/actions/add-memory" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "inputData": "string",
  "teamName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/crewMem/latest/actions/add-memory', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "inputData": "string",
    "teamName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Member email |
| `inputData` | string | yes | Memory content to add |
| `teamName` | string | yes | Target team name |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addedMemoryCount": 1,
      "data": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addedMemoryCount` | number |  |
| `data` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native CrewMem API, this operation is `POST /api/v1/memory/add` (base URL `https://crewmem.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-memory.md) for the provider-specific parameters and requirements.

