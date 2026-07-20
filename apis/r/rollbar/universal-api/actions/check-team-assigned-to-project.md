# Rollbar: Check Team Assigned To Project

Retrieves whether a team is assigned to a Rollbar project.

```
GET https://connect.mindcloud.co/v1/universal/rollbar/latest/actions/check-team-assigned-to-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rollbar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rollbar/latest/actions/check-team-assigned-to-project?connectionId=$CONNECTION_ID&projectId=1&teamId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1",
  "teamId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rollbar/latest/actions/check-team-assigned-to-project?${params}`, {
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
| `projectId` | number | yes | Rollbar project identifier. |
| `teamId` | number | yes | Rollbar team identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "err": 1,
      "result": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `err` | number |  |
| `result` | object |  |

## Native endpoint

Through the native Rollbar API, this operation is `GET /project/:projectId/team/:teamId` (base URL `https://api.rollbar.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-team-assigned-to-project.md) for the provider-specific parameters and requirements.

