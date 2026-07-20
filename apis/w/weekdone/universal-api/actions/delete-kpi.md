# Weekdone: Delete KPI

Deletes an existing KPI from Weekdone.

```
DELETE https://connect.mindcloud.co/v1/universal/weekdone/latest/actions/delete-kpi
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Weekdone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/weekdone/latest/actions/delete-kpi?connectionId=$CONNECTION_ID&kpiId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "kpiId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weekdone/latest/actions/delete-kpi?${params}`, {
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
| `kpiId` | number | yes |  |

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

Through the native Weekdone API, this operation is `DELETE kpi/:kpiId` (base URL `https://api.weekdone.com/1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-kpi.md) for the provider-specific parameters and requirements.

