# Benchmark Email: Update Contact

Updates a contact in a Benchmark Email contact list.

```
PUT https://connect.mindcloud.co/v1/universal/benchmarkEmail/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Benchmark Email `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/benchmarkEmail/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "string",
  "data": {},
  "listId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/benchmarkEmail/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "string",
    "data": {},
    "listId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | string | yes | Benchmark contact ID. |
| `data` | object | yes | Contact payload object. |
| `listId` | string | yes | Benchmark contact list ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Benchmark Email API returns.

## Native endpoint

Through the native Benchmark Email API, this operation is `PATCH /Contact/:listId/ContactDetails/:contactId` (base URL `https://clientapi.benchmarkemail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

