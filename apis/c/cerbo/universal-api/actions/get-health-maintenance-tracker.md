# Cerbo: Get Health Maintenance Tracker

Retrieves health maintenance tracker details from Cerbo.

```
GET https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/get-health-maintenance-tracker
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/get-health-maintenance-tracker?connectionId=$CONNECTION_ID&health_maintenance_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "health_maintenance_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/get-health-maintenance-tracker?${params}`, {
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
| `health_maintenance_id` | number | yes | The ID of the health maintenance tracker to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addedby": "string",
      "applies_to": "string",
      "created": "string",
      "description": "string",
      "end_age": 1,
      "frequency": "string",
      "icd_codes": "string",
      "id": "string",
      "name": "Ava Chen",
      "object": "string",
      "overrides": "string",
      "sex": "string",
      "start_age": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addedby` | string |  |
| `applies_to` | string |  |
| `created` | string |  |
| `description` | string |  |
| `end_age` | number |  |
| `frequency` | string |  |
| `icd_codes` | string |  |
| `id` | string |  |
| `name` | string |  |
| `object` | string |  |
| `overrides` | string |  |
| `sex` | string |  |
| `start_age` | number |  |

## Native endpoint

Through the native Cerbo API, this operation is `GET /health_maintenance/:health_maintenance_id` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-health-maintenance-tracker.md) for the provider-specific parameters and requirements.

