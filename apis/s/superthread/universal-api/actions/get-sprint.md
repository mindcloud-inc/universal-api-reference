# Superthread: Get Sprint



```
GET https://connect.mindcloud.co/v1/universal/superthread/latest/actions/get-sprint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Superthread `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superthread/latest/actions/get-sprint?connectionId=$CONNECTION_ID&teamId=string&sprintId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string",
  "sprintId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superthread/latest/actions/get-sprint?${params}`, {
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
| `teamId` | string | yes |  |
| `sprintId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "sprint": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `sprint` | object |  |

## Native endpoint

Through the native Superthread API, this operation is `GET /:team_id/sprints/:sprint_id` (base URL `https://api.superthread.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sprint.md) for the provider-specific parameters and requirements.

