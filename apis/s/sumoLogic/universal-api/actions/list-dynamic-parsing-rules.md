# Sumo Logic: List Dynamic Parsing Rules

Retrieves dynamic parsing rules from your Sumo Logic organization.

```
GET https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-dynamic-parsing-rules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumo Logic `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-dynamic-parsing-rules?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-dynamic-parsing-rules?${params}`, {
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
      "createdAt": "string",
      "createdBy": "string",
      "enabled": true,
      "id": "string",
      "isSystemRule": true,
      "modifiedAt": "string",
      "modifiedBy": "string",
      "name": "Ava Chen",
      "scope": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `createdBy` | string |  |
| `enabled` | boolean |  |
| `id` | string |  |
| `isSystemRule` | boolean |  |
| `modifiedAt` | string |  |
| `modifiedBy` | string |  |
| `name` | string |  |
| `scope` | string |  |

## Native endpoint

Through the native Sumo Logic API, this operation is `GET /v1/dynamicParsingRules` (base URL `https://api.sumologic.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-dynamic-parsing-rules.md) for the provider-specific parameters and requirements.

