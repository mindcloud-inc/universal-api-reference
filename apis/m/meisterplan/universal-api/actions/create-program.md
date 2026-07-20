# Meisterplan: Create Program

Creates a new program in Meisterplan.

```
POST https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/create-program
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Meisterplan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/create-program" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "scenarioId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/meisterplan/latest/actions/create-program', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "scenarioId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `scenarioId` | string | yes | Internal Meisterplan scenario identifier. |
| `name` | string | yes | Program name. |
| `programKey` | string | no | Unique Meisterplan program key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "finish": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "programKey": "string",
      "rankCategory": {
        "value": "string"
      },
      "start": "2026-05-07T12:00:00.000Z",
      "status": {
        "value": "string"
      },
      "viewUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `finish` | date | Program finish date |
| `id` | string | Program ID |
| `name` | string | Program name |
| `programKey` | string | Program key |
| `rankCategory.value` | string | Rank category |
| `start` | date | Program start date |
| `status.value` | string | Program status |
| `viewUrl` | string | View URL |

## Native endpoint

Through the native Meisterplan API, this operation is `POST /scenarios/:scenarioId/programs` (base URL `https://api.us.meisterplan.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-program.md) for the provider-specific parameters and requirements.

