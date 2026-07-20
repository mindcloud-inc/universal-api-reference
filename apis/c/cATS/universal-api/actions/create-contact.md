# CATS: Create Contact

Creates a new contact in CATS.

```
POST https://connect.mindcloud.co/v1/universal/cATS/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CATS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cATS/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "MindCloud",
  "lastName": "Stage3 Contact",
  "ownerId": "595927",
  "companyId": "23102956"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cATS/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "MindCloud",
    "lastName": "Stage3 Contact",
    "ownerId": "595927",
    "companyId": "23102956"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | yes | The contact first name. Example: `MindCloud`. |
| `lastName` | string | yes | The contact last name. Example: `Stage3 Contact`. |
| `ownerId` | number | yes | The owning user ID. Example: `595927`. |
| `companyId` | number | yes | The company ID this contact belongs to. Example: `23102956`. |
| `checkDuplicate` | boolean | no | Throw an error instead of creating a duplicate when true. Example: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CATS API returns.

## Native endpoint

Through the native CATS API, this operation is `POST /contacts` (base URL `https://api.catsone.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

