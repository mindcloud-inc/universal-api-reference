# Sumo Logic: List Data Masking Rules

Retrieves data masking rules from your Sumo Logic organization.

```
GET https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-data-masking-rules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumo Logic `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-data-masking-rules?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-data-masking-rules?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "description": "string",
      "enabled": true,
      "id": "string",
      "maskString": "string",
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "modifiedBy": "string",
      "name": "Ava Chen",
      "regexPattern": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `description` | string |  |
| `enabled` | boolean |  |
| `id` | string |  |
| `maskString` | string |  |
| `modifiedAt` | date |  |
| `modifiedBy` | string |  |
| `name` | string |  |
| `regexPattern` | string |  |

## Native endpoint

Through the native Sumo Logic API, this operation is `GET /v1/dataMaskingRules` (base URL `https://api.sumologic.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-data-masking-rules.md) for the provider-specific parameters and requirements.

