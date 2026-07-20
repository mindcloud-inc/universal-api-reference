# Podscan: Get Team Alert Group

Retrieves a team alert group from Podscan.

```
GET https://connect.mindcloud.co/v1/universal/podscan/latest/actions/get-team-alert-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Podscan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/podscan/latest/actions/get-team-alert-group?connectionId=$CONNECTION_ID&group=string&team=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "group": "string",
  "team": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/podscan/latest/actions/get-team-alert-group?${params}`, {
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
| `group` | string | yes | The alert group ID. |
| `team` | string | yes | The team ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alert_group": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alert_group` | object |  |

## Native endpoint

Through the native Podscan API, this operation is `GET /teams/{team}/alert-groups/{group}` (base URL `https://podscan.fm/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-team-alert-group.md) for the provider-specific parameters and requirements.

