# Status Hero: Remove team absence



```
DELETE https://connect.mindcloud.co/v1/universal/statusHero/latest/actions/remove-team-absence
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Status Hero `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/statusHero/latest/actions/remove-team-absence?connectionId=$CONNECTION_ID&date=2026-12-31" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "date": "2026-12-31"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statusHero/latest/actions/remove-team-absence?${params}`, {
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
| `date` | string | yes | Team-wide absence date in YYYY-MM-DD format. Example: `2026-12-31`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native Status Hero API, this operation is `DELETE /team_absences/:date` (base URL `https://service.statushero.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-team-absence.md) for the provider-specific parameters and requirements.

