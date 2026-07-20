# Unleash: [Beta] Delete A Milestone Progression

Deletes a milestone progression from Unleash.

```
DELETE https://connect.mindcloud.co/v1/universal/unleash/latest/actions/deletemilestoneprogression
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unleash `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/unleash/latest/actions/deletemilestoneprogression?connectionId=$CONNECTION_ID&project=string&featureName=Ava%20Chen&environment=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project": "string",
  "featureName": "Ava Chen",
  "environment": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unleash/latest/actions/deletemilestoneprogression?${params}`, {
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
| `project` | string | yes | Required path parameter. |
| `featureName` | string | yes | Required path parameter. |
| `environment` | string | yes | Required path parameter. |
| `id` | string | yes | Required path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "message": "string",
      "name": "Ava Chen",
      "success": true,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Creation timestamp. |
| `description` | string | Resource description. |
| `id` | string | Resource identifier. |
| `message` | string | Response message. |
| `name` | string | Resource name. |
| `success` | boolean | Whether the operation succeeded. |
| `updatedAt` | date | Last update timestamp. |

## Native endpoint

Through the native Unleash API, this operation is `DELETE /api/admin/projects/{project}/features/{featureName}/environments/{environment}/progressions/{id}` (base URL `https://us.app.getunleash.io/uspp0456`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/deletemilestoneprogression.md) for the provider-specific parameters and requirements.

