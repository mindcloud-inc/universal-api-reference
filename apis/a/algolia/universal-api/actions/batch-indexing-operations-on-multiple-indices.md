# Algolia: Batch Indexing Operations on Multiple Indices

Runs batch indexing operations on multiple Algolia indices.

```
POST https://connect.mindcloud.co/v1/universal/algolia/latest/actions/batch-indexing-operations-on-multiple-indices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Algolia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/algolia/latest/actions/batch-indexing-operations-on-multiple-indices" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "requests[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/algolia/latest/actions/batch-indexing-operations-on-multiple-indices', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "requests[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `requests[]` | array<object> | yes | Batch requests for one or more indices. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "objectIDs": [
        "string"
      ],
      "taskID": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `objectIDs` | array<string> |  |
| `taskID` | object |  |

## Native endpoint

Through the native Algolia API, this operation is `POST /1/indexes/*/batch` (base URL `https://{{credentials.applicationId}}.algolia.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-indexing-operations-on-multiple-indices.md) for the provider-specific parameters and requirements.

