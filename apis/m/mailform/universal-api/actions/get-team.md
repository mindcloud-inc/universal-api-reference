# Mailform: Get Team



```
GET https://connect.mindcloud.co/v1/universal/mailform/latest/actions/get-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailform/latest/actions/get-team?connectionId=$CONNECTION_ID&teamId=2543d0ff-fff1-4f71-8993-f2c5701f6b6f" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "2543d0ff-fff1-4f71-8993-f2c5701f6b6f"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailform/latest/actions/get-team?${params}`, {
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
| `teamId` | string | yes | ID of the team to retrieve. Example: `2543d0ff-fff1-4f71-8993-f2c5701f6b6f`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Mailform API returns.

## Native endpoint

Through the native Mailform API, this operation is `GET /teams/:team_id` (base URL `https://www.mailform.io/app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-team.md) for the provider-specific parameters and requirements.

