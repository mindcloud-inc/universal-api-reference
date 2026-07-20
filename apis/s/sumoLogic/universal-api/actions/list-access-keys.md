# Sumo Logic: List Access Keys

Retrieves access keys from your Sumo Logic account.

```
GET https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-access-keys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumo Logic `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-access-keys?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-access-keys?${params}`, {
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
      "corsHeaders": [
        "string"
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "disabled": true,
      "effectiveScopes": [
        "string"
      ],
      "id": "string",
      "label": "string",
      "lastUsed": "2026-05-07T12:00:00.000Z",
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "modifiedBy": "string",
      "scopes": [
        "string"
      ],
      "serviceAccountId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `corsHeaders[]` | string |  |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `disabled` | boolean |  |
| `effectiveScopes[]` | string |  |
| `id` | string |  |
| `label` | string |  |
| `lastUsed` | date |  |
| `modifiedAt` | date |  |
| `modifiedBy` | string |  |
| `scopes[]` | string |  |
| `serviceAccountId` | string |  |

## Native endpoint

Through the native Sumo Logic API, this operation is `GET /v1/accessKeys` (base URL `https://api.sumologic.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-access-keys.md) for the provider-specific parameters and requirements.

