# SIGNL4: Get Team Setup Progress

Retrieves team setup progress from SIGNL4.

```
GET https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-team-setup-progress
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SIGNL4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-team-setup-progress?connectionId=$CONNECTION_ID&teamId=sample-team-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "sample-team-id"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/get-team-setup-progress?${params}`, {
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
| `teamId` | string | yes | SIGNL4 team ID. Example: `sample-team-id`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedSteps": [
        "string"
      ],
      "teamId": "string",
      "timestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedSteps` | array<string> |  |
| `teamId` | string |  |
| `timestamp` | date |  |

## Native endpoint

Through the native SIGNL4 API, this operation is `GET /v2/teams/{teamId}/setupProgress` (base URL `https://connect.signl4.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-team-setup-progress.md) for the provider-specific parameters and requirements.

