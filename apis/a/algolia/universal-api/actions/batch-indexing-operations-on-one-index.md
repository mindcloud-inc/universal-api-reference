# Algolia: Batch Indexing Operations on One Index

Runs batch indexing operations on one Algolia index.

```
POST https://connect.mindcloud.co/v1/universal/algolia/latest/actions/batch-indexing-operations-on-one-index
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Algolia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/algolia/latest/actions/batch-indexing-operations-on-one-index" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "indexName": "Ava Chen",
  "requests[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/algolia/latest/actions/batch-indexing-operations-on-one-index', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "indexName": "Ava Chen",
    "requests[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `indexName` | string | yes | The name of the Algolia index. |
| `requests[]` | array<object> | yes | Batch requests for the index. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "objectIDs": [
        "string"
      ],
      "taskID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `objectIDs` | array<string> |  |
| `taskID` | number |  |

## Native endpoint

Through the native Algolia API, this operation is `POST /1/indexes/:indexName/batch` (base URL `https://{{credentials.applicationId}}.algolia.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-indexing-operations-on-one-index.md) for the provider-specific parameters and requirements.

