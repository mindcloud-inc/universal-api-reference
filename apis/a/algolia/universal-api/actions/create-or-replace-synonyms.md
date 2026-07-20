# Algolia: Create or Replace Synonyms

Creates or replaces multiple synonyms in Algolia.

```
POST https://connect.mindcloud.co/v1/universal/algolia/latest/actions/create-or-replace-synonyms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Algolia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/algolia/latest/actions/create-or-replace-synonyms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "indexName": "Ava Chen",
  "synonymObjects[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/algolia/latest/actions/create-or-replace-synonyms', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "indexName": "Ava Chen",
    "synonymObjects[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `indexName` | string | yes | Name of the index on which to perform the batch operation. |
| `replaceExistingSynonyms` | boolean | no | Whether to replace all synonyms in the index with the ones in this request. |
| `synonymObjects[]` | array<object> | yes | Array of synonym objects to create or replace. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `forwardToReplicas` | boolean | no | Whether changes are applied to replica indices. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "taskID": 1,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `taskID` | number | Algolia task identifier for the batch synonym write. |
| `updatedAt` | string | RFC 3339 timestamp when the batch synonym write completed. |

## Native endpoint

Through the native Algolia API, this operation is `POST /1/indexes/:indexName/synonyms/batch` (base URL `https://{{credentials.applicationId}}.algolia.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-replace-synonyms.md) for the provider-specific parameters and requirements.

