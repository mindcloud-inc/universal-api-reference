# Algolia: Delete All Rules

Deletes all rules from an Algolia index.

```
DELETE https://connect.mindcloud.co/v1/universal/algolia/latest/actions/delete-all-rules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Algolia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/algolia/latest/actions/delete-all-rules?connectionId=$CONNECTION_ID&indexName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "indexName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/algolia/latest/actions/delete-all-rules?${params}`, {
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
| `indexName` | string | yes | Index name from which to delete all rules. |

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
| `taskID` | number |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Algolia API, this operation is `POST /1/indexes/:indexName/rules/clear` (base URL `https://{{credentials.applicationId}}.algolia.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-all-rules.md) for the provider-specific parameters and requirements.

