# Status Hero: Add member absence



```
POST https://connect.mindcloud.co/v1/universal/statusHero/latest/actions/add-member-absence
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Status Hero `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/statusHero/latest/actions/add-member-absence" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "1e1a64b7-54e0-4f5f-a492-7edc28c86094",
  "date": "2026-12-31"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/statusHero/latest/actions/add-member-absence', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "1e1a64b7-54e0-4f5f-a492-7edc28c86094",
    "date": "2026-12-31"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The member ID or slug to mark absent. Example: `1e1a64b7-54e0-4f5f-a492-7edc28c86094`. |
| `date` | string | yes | Absence date in YYYY-MM-DD format. Example: `2026-12-31`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "member": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date |  |
| `member` | object |  |

## Native endpoint

Through the native Status Hero API, this operation is `POST /member_absences/:id` (base URL `https://service.statushero.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-member-absence.md) for the provider-specific parameters and requirements.

