# Virtually: List Triggers

Retrieves triggers from your Virtually workspace.

```
GET https://connect.mindcloud.co/v1/universal/virtually/latest/actions/list-triggers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Virtually `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/virtually/latest/actions/list-triggers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/virtually/latest/actions/list-triggers?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "clauses": [
        {}
      ],
      "createdBy": "string",
      "cronSchedule": "string",
      "description": "string",
      "logicalOp": "string",
      "name": "Ava Chen",
      "orgId": "string",
      "triggerId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clauses` | array<object> |  |
| `createdBy` | string |  |
| `cronSchedule` | string |  |
| `description` | string |  |
| `logicalOp` | string |  |
| `name` | string |  |
| `orgId` | string |  |
| `triggerId` | string |  |

## Native endpoint

Through the native Virtually API, this operation is `GET /api/v2/orgs/:orgId/triggers` (base URL `https://app.tryvirtually.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-triggers.md) for the provider-specific parameters and requirements.

