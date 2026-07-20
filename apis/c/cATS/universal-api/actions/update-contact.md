# CATS: Update Contact

Updates an existing contact in CATS.

```
PUT https://connect.mindcloud.co/v1/universal/cATS/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CATS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cATS/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "47087446",
  "firstName": "MindCloud",
  "lastName": "Stage3 Contact Updated",
  "ownerId": "595927",
  "companyId": "23102956"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cATS/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "47087446",
    "firstName": "MindCloud",
    "lastName": "Stage3 Contact Updated",
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
| `id` | number | yes | The ID of the contact to update. Example: `47087446`. |
| `firstName` | string | yes | The contact first name. Example: `MindCloud`. |
| `lastName` | string | yes | The contact last name. Example: `Stage3 Contact Updated`. |
| `ownerId` | number | yes | The owning user ID. Example: `595927`. |
| `companyId` | number | yes | The company ID this contact belongs to. Example: `23102956`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CATS API returns.

## Native endpoint

Through the native CATS API, this operation is `PUT /contacts/:id` (base URL `https://api.catsone.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

