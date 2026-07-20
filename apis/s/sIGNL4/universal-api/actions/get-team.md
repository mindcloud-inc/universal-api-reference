# SIGNL4: Get Team

Retrieves a team from SIGNL4 by ID.

```
GET https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SIGNL4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-team?connectionId=$CONNECTION_ID&teamId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-team?${params}`, {
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
| `teamId` | string | yes | ID of the team that should be retrieved. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "externalName": "Ava Chen",
      "id": "string",
      "imageLastModified": "2026-05-07T12:00:00.000Z",
      "imageWebLastModified": "2026-05-07T12:00:00.000Z",
      "memberIds": [
        "string"
      ],
      "name": "Ava Chen",
      "options": 1,
      "subscriptionId": "string",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `externalName` | string |  |
| `id` | string |  |
| `imageLastModified` | date |  |
| `imageWebLastModified` | date |  |
| `memberIds` | array<string> |  |
| `name` | string |  |
| `options` | number |  |
| `subscriptionId` | string |  |
| `timezone` | string |  |

## Native endpoint

Through the native SIGNL4 API, this operation is `GET /v2/teams/{teamId}` (base URL `https://connect.signl4.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-team.md) for the provider-specific parameters and requirements.

