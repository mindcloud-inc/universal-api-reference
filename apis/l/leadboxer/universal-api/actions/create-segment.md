# Leadboxer: Create Segment

Creates a new segment in Leadboxer.

```
POST https://connect.mindcloud.co/v1/universal/leadboxer/latest/actions/create-segment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadboxer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/leadboxer/latest/actions/create-segment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "name": "Ava Chen",
  "accountId": "string",
  "datasetId": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/leadboxer/latest/actions/create-segment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "name": "Ava Chen",
    "accountId": "string",
    "datasetId": "string",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | The user email address. |
| `name` | string | yes | Segment name. |
| `accountId` | string | yes | The Leadboxer account ID. |
| `datasetId` | string | yes | The dataset ID. |
| `type` | string | yes | Segment visibility type. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Leadboxer API returns.

## Native endpoint

Through the native Leadboxer API, this operation is `POST /v1/segments` (base URL `https://data.leadboxer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-segment.md) for the provider-specific parameters and requirements.

