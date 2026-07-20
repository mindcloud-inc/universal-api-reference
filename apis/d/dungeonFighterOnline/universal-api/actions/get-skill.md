# Dungeon Fighter Online: Get Skill

Retrieves skill details from Dungeon Fighter Online.

```
GET https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/get-skill
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dungeon Fighter Online `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/get-skill?connectionId=$CONNECTION_ID&jobId=string&skillId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string",
  "skillId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/get-skill?${params}`, {
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
| `skillId` | string | yes | Dungeon Fighter skill ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "desc": "string",
      "name": "Ava Chen",
      "requiredLevel": 1,
      "skillId": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `desc` | string |  |
| `name` | string |  |
| `requiredLevel` | number |  |
| `skillId` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Dungeon Fighter Online API, this operation is `GET /df/skills/:jobId/:skillId` (base URL `https://api.neople.co.kr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-skill.md) for the provider-specific parameters and requirements.

