# Insightful: Get Team

Retrieves a team from your Insightful account.

```
GET https://connect.mindcloud.co/v1/universal/insightful/latest/actions/get-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insightful `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightful/latest/actions/get-team?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/insightful/latest/actions/get-team?${params}`, {
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
| `id` | string | yes | The team ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "default": true,
      "description": "string",
      "id": "string",
      "ignoreNeutral": true,
      "ignoreProductive": true,
      "ignoreUnproductive": true,
      "ignoreUnreviewed": true,
      "modelName": "Ava Chen",
      "name": "Ava Chen",
      "organizationId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `default` | boolean |  |
| `description` | string |  |
| `id` | string |  |
| `ignoreNeutral` | boolean |  |
| `ignoreProductive` | boolean |  |
| `ignoreUnproductive` | boolean |  |
| `ignoreUnreviewed` | boolean |  |
| `modelName` | string |  |
| `name` | string |  |
| `organizationId` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Insightful API, this operation is `GET /team/:id` (base URL `https://app.insightful.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-team.md) for the provider-specific parameters and requirements.

