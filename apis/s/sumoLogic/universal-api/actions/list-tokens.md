# Sumo Logic: List Tokens

Retrieves tokens from your Sumo Logic token library.

```
GET https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-tokens
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumo Logic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-tokens?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-tokens?${params}`, {
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
      "id": "string",
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "modifiedBy": "string",
      "name": "Ava Chen",
      "status": "string",
      "type": "string",
      "version": 1
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
| `id` | string |  |
| `modifiedAt` | date |  |
| `modifiedBy` | string |  |
| `name` | string |  |
| `status` | string |  |
| `type` | string |  |
| `version` | number |  |

## Native endpoint

Through the native Sumo Logic API, this operation is `GET /v1/tokens` (base URL `https://api.sumologic.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tokens.md) for the provider-specific parameters and requirements.

