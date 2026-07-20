# Dungeon Fighter Online: List Skills

Retrieves a job's skills from Dungeon Fighter Online.

```
GET https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/list-skills
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dungeon Fighter Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/list-skills?connectionId=$CONNECTION_ID&jobId=string&jobGrowId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string",
  "jobGrowId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/list-skills?${params}`, {
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
| `jobId` | string | yes | Dungeon Fighter job ID. |
| `jobGrowId` | string | yes | Optional job growth ID for filtering the skill list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "requiredLevel": 1,
      "skillId": "string",
      "skills": [
        {}
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `requiredLevel` | number |  |
| `skillId` | string |  |
| `skills` | array<object> |  |
| `type` | string |  |

## Native endpoint

Through the native Dungeon Fighter Online API, this operation is `GET /df/skills/:jobId` (base URL `https://api.neople.co.kr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-skills.md) for the provider-specific parameters and requirements.

