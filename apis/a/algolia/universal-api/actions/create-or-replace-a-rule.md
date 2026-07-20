# Algolia: Create or Replace a Rule

Creates or replaces a rule in Algolia.

```
POST https://connect.mindcloud.co/v1/universal/algolia/latest/actions/create-or-replace-a-rule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Algolia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/algolia/latest/actions/create-or-replace-a-rule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "indexName": "Ava Chen",
  "objectId": "string",
  "bodyObjectId": "string",
  "consequence": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/algolia/latest/actions/create-or-replace-a-rule', {
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
    "consequence": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `indexName` | string | yes | Name of the index on which to perform the operation. |
| `objectId` | string | yes | Unique identifier of the rule object in the request path. |
| `bodyObjectId` | string | yes | Unique identifier of the rule object in the request body. |
| `consequence` | object | yes | Effect of the rule as a JSON object. |
| `conditions[]` | array<object> | no | Conditions that trigger the rule as an array of JSON objects. |
| `description` | string | no | Description to help identify this rule. |
| `enabled` | boolean | no | Whether the rule is enabled. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `forwardToReplicas` | boolean | no | Whether changes are applied to replica indices. |
| `tags[]` | array<string> | no | Tags attached to the rule. |
| `validity[]` | array<object> | no | Validity windows for the rule. |
| `scope` | string | no | The scope of the rule. |

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
| `taskID` | number | Algolia task identifier for the rule write. |
| `updatedAt` | string | RFC 3339 timestamp when the rule write completed. |

## Native endpoint

Through the native Algolia API, this operation is `PUT /1/indexes/:indexName/rules/:objectID` (base URL `https://{{credentials.applicationId}}.algolia.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-replace-a-rule.md) for the provider-specific parameters and requirements.

