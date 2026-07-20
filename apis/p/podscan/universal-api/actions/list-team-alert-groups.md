# Podscan: List Team Alert Groups

Retrieves alert groups for a team from Podscan.

```
GET https://connect.mindcloud.co/v1/universal/podscan/latest/actions/list-team-alert-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Podscan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/podscan/latest/actions/list-team-alert-groups?connectionId=$CONNECTION_ID&team=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "team": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/podscan/latest/actions/list-team-alert-groups?${params}`, {
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
| `team` | string | yes | The team ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alert_groups": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alert_groups` | array<object> |  |

## Native endpoint

Through the native Podscan API, this operation is `GET /teams/{team}/alert-groups` (base URL `https://podscan.fm/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-team-alert-groups.md) for the provider-specific parameters and requirements.

