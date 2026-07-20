# Onfleet: Get Team

Retrieves a team from Onfleet.

```
GET https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/get-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Onfleet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/get-team?connectionId=$CONNECTION_ID&teamId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/get-team?${params}`, {
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
| `teamId` | string | yes | The Onfleet team ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "enableSelfAssignment": true,
      "id": "string",
      "managers": [
        "string"
      ],
      "name": "Ava Chen",
      "tasks": [
        "string"
      ],
      "workers": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `enableSelfAssignment` | boolean |  |
| `id` | string |  |
| `managers` | array<string> |  |
| `name` | string |  |
| `tasks` | array |  |
| `workers` | array<string> |  |

## Native endpoint

Through the native Onfleet API, this operation is `GET /teams/:teamId` (base URL `https://onfleet.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-team.md) for the provider-specific parameters and requirements.

