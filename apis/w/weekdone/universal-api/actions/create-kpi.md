# Weekdone: Create KPI

Creates a new KPI in Weekdone.

```
POST https://connect.mindcloud.co/v1/universal/weekdone/latest/actions/create-kpi
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weekdone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/weekdone/latest/actions/create-kpi" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "description": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weekdone/latest/actions/create-kpi', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "description": "string",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `decimals` | number | no |  |
| `departmentId` | number | no |  |
| `description` | string | yes |  |
| `maxval` | number | no |  |
| `startval` | number | no |  |
| `teamId` | number | no |  |
| `type` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |

## Native endpoint

Through the native Weekdone API, this operation is `POST kpi` (base URL `https://api.weekdone.com/1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-kpi.md) for the provider-specific parameters and requirements.

