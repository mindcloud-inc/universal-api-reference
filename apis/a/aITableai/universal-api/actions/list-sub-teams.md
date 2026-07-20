# AITable.ai: List Sub Teams

Retrieves sub teams from AITable.ai.

```
GET https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/list-sub-teams
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AITable.ai `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/list-sub-teams?connectionId=$CONNECTION_ID&limit=25&offset=0&spaceId=string&unitId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "spaceId": "string",
  "unitId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aITableai/latest/actions/list-sub-teams?${params}`, {
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
| `spaceId` | string | yes | AITable space ID containing the parent team. |
| `unitId` | string | yes | AITable parent team unit ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pageNum": 1,
      "pageSize": 1,
      "teams": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pageNum` | number | Current page number. |
| `pageSize` | number | Page size. |
| `teams` | array<object> | Sub teams. |
| `total` | number | Total sub teams. |

## Native endpoint

Through the native AITable.ai API, this operation is `GET /fusion/v1/spaces/:spaceId/teams/:unitId/children` (base URL `https://aitable.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sub-teams.md) for the provider-specific parameters and requirements.

