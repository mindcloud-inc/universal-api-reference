# Grain: Unshare Recording from Team

Unshares a recording from a team in Grain.

```
DELETE https://connect.mindcloud.co/v1/universal/grain/latest/actions/unshare-recording-from-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/grain/latest/actions/unshare-recording-from-team?connectionId=$CONNECTION_ID&recording_id=string&team_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "recording_id": "string",
  "team_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grain/latest/actions/unshare-recording-from-team?${params}`, {
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
| `recording_id` | list<string> | yes |  |
| `team_id` | list<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Grain API, this operation is `DELETE /v2/recordings/:recording_id/teams/:team_id` (base URL `https://api.grain.com/_/public-api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unshare-recording-from-team.md) for the provider-specific parameters and requirements.

