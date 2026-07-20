# Cerbo: Get Custom Vital Definition

Retrieves custom vital definition details from Cerbo.

```
GET https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/get-custom-vital-definition
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/get-custom-vital-definition?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/get-custom-vital-definition?${params}`, {
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
| `vital_id` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addedby": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "dashboard_active": true,
      "id": 1,
      "name": "Ava Chen",
      "name_full": "Ava Chen",
      "nicknames": "Ava Chen",
      "normal_high": "string",
      "normal_low": "string",
      "notes": "string",
      "object": "string",
      "unit_type": "string",
      "units": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addedby` | number |  |
| `created` | date |  |
| `dashboard_active` | boolean |  |
| `id` | number |  |
| `name` | string |  |
| `name_full` | string |  |
| `nicknames` | string |  |
| `normal_high` | string |  |
| `normal_low` | string |  |
| `notes` | string |  |
| `object` | string |  |
| `unit_type` | string |  |
| `units` | string |  |

## Native endpoint

Through the native Cerbo API, this operation is `GET /vitals/:vital_id` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-custom-vital-definition.md) for the provider-specific parameters and requirements.

