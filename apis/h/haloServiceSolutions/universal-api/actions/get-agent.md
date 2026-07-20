# Halo Service Solutions: Get Agent

Retrieves an agent from Halo Service Solutions.

```
GET https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/get-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Halo Service Solutions `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/get-agent?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/haloServiceSolutions/latest/actions/get-agent?${params}`, {
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
| `id` | number | yes | Agent ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "datecreated": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstname": "Ava",
      "guid": "string",
      "id": 1,
      "is_agent": true,
      "isdisabled": true,
      "name": "Ava Chen",
      "surname": "Ava Chen",
      "team": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `datecreated` | date |  |
| `email` | string |  |
| `firstname` | string |  |
| `guid` | string |  |
| `id` | number |  |
| `is_agent` | boolean |  |
| `isdisabled` | boolean |  |
| `name` | string |  |
| `surname` | string |  |
| `team` | string |  |

## Native endpoint

Through the native Halo Service Solutions API, this operation is `GET /Agent/:id` (base URL `https://mindcloud.halopsa.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-agent.md) for the provider-specific parameters and requirements.

