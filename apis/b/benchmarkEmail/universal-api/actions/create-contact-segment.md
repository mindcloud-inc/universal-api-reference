# Benchmark Email: Create Contact Segment

Creates a contact segment in Benchmark Email.

```
POST https://connect.mindcloud.co/v1/universal/benchmarkEmail/latest/actions/create-contact-segment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Benchmark Email `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/benchmarkEmail/latest/actions/create-contact-segment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactIds": "string",
  "listId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/benchmarkEmail/latest/actions/create-contact-segment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactIds": "string",
    "listId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactIds` | string<string> | yes | Contact IDs to include in the segment. |
| `listId` | string | yes | Benchmark contact list ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Benchmark Email API returns.

## Native endpoint

Through the native Benchmark Email API, this operation is `POST /Contact/:listId/Segments` (base URL `https://clientapi.benchmarkemail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact-segment.md) for the provider-specific parameters and requirements.

