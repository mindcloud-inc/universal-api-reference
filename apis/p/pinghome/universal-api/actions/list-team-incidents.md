# Pinghome: List Team Incidents

Retrieves team incidents from Pinghome.

```
GET https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/list-team-incidents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinghome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/list-team-incidents?connectionId=$CONNECTION_ID&teamId=2a85fda9-2f9b-4daf-b040-f30a835cafa5" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "2a85fda9-2f9b-4daf-b040-f30a835cafa5"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/list-team-incidents?${params}`, {
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
| `teamId` | string | yes | Team ID for incident retrieval. Example: `2a85fda9-2f9b-4daf-b040-f30a835cafa5`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pinghome API returns.

## Native endpoint

Through the native Pinghome API, this operation is `GET /incident-query/v1/team/:id/incidents` (base URL `https://api.pinghome.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-team-incidents.md) for the provider-specific parameters and requirements.

