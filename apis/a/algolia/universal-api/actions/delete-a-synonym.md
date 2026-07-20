# Algolia: Delete a Synonym

Deletes an existing synonym from Algolia.

```
DELETE https://connect.mindcloud.co/v1/universal/algolia/latest/actions/delete-a-synonym
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Algolia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/algolia/latest/actions/delete-a-synonym?connectionId=$CONNECTION_ID&indexName=Ava%20Chen&objectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "indexName": "Ava Chen",
  "objectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/algolia/latest/actions/delete-a-synonym?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `indexName` | string | yes | Index name that contains the synonym. |
| `objectId` | string | yes | Unique identifier of the synonym object. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `forwardToReplicas` | boolean | no | Whether to forward the deletion to replicas. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deletedAt": "string",
      "taskID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deletedAt` | string |  |
| `taskID` | number |  |

## Native endpoint

Through the native Algolia API, this operation is `DELETE /1/indexes/:indexName/synonyms/:objectID` (base URL `https://{{credentials.applicationId}}.algolia.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-a-synonym.md) for the provider-specific parameters and requirements.

