# CATS: Create Candidate

Creates a new candidate in CATS.

```
POST https://connect.mindcloud.co/v1/universal/cATS/latest/actions/create-candidate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CATS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cATS/latest/actions/create-candidate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "MindCloud",
  "lastName": "Tester"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cATS/latest/actions/create-candidate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "MindCloud",
    "lastName": "Tester"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | yes | The candidate first name. Example: `MindCloud`. |
| `lastName` | string | yes | The candidate last name. Example: `Tester`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CATS API returns.

## Native endpoint

Through the native CATS API, this operation is `POST /candidates` (base URL `https://api.catsone.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-candidate.md) for the provider-specific parameters and requirements.

