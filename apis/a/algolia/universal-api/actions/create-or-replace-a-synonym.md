# Algolia: Create or Replace a Synonym

Creates or replaces a synonym in Algolia.

```
POST https://connect.mindcloud.co/v1/universal/algolia/latest/actions/create-or-replace-a-synonym
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Algolia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/algolia/latest/actions/create-or-replace-a-synonym" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "indexName": "Ava Chen",
  "objectId": "string",
  "bodyObjectId": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/algolia/latest/actions/create-or-replace-a-synonym', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "indexName": "Ava Chen",
    "objectId": "string",
    "bodyObjectId": "string",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `indexName` | string | yes | Name of the index on which to perform the operation. |
| `objectId` | string | yes | Unique identifier of the synonym object in the request path. |
| `bodyObjectId` | string | yes | Unique identifier of the synonym object in the request body. |
| `type` | string | yes | Synonym type. |
| `synonyms[]` | array<string> | no | Words or phrases considered equivalent. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `forwardToReplicas` | boolean | no | Whether changes are applied to replica indices. |
| `input` | string | no | Query word or phrase for one-way synonyms. |
| `word` | string | no | Query word or phrase for alternative corrections. |
| `corrections[]` | array<string> | no | Words to be matched in records for alternative corrections. |
| `placeholder` | string | no | Placeholder token to put inside records. |
| `replacements[]` | array<string> | no | Query words that will match the placeholder token. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
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
| `id` | string | Unique identifier of the synonym object. |
| `taskID` | number | Algolia task identifier for the synonym write. |
| `updatedAt` | string | RFC 3339 timestamp when the synonym was updated. |

## Native endpoint

Through the native Algolia API, this operation is `PUT /1/indexes/:indexName/synonyms/:objectID` (base URL `https://{{credentials.applicationId}}.algolia.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-replace-a-synonym.md) for the provider-specific parameters and requirements.

