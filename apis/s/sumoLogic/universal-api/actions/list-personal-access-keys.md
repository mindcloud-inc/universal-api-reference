# Sumo Logic: List Personal Access Keys

Retrieves access keys owned by your Sumo Logic user.

```
GET https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-personal-access-keys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumo Logic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-personal-access-keys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-personal-access-keys?${params}`, {
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

Through the native Sumo Logic API, this operation is `GET /v1/accessKeys/personal` (base URL `https://api.sumologic.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-personal-access-keys.md) for the provider-specific parameters and requirements.

