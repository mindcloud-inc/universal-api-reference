# Cerbo: List Patient Custom Vitals

Retrieves patient custom vitals from Cerbo.

```
GET https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-patient-custom-vitals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-patient-custom-vitals?connectionId=$CONNECTION_ID&patient_id=1&vital_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "patient_id": "1",
  "vital_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-patient-custom-vitals?${params}`, {
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
| `patient_id` | number | yes | ID of patient |
| `vital_id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "abnormal": true,
      "addedby": 1,
      "comments": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "date_taken": "2026-05-07T12:00:00.000Z",
      "encounter_id": 1,
      "id": 1,
      "object": "string",
      "order_id": 1,
      "pt_id": 1,
      "units": "string",
      "url_encounter": "https://example.com",
      "url_order": "https://example.com",
      "value": "string",
      "vital_id": 1,
      "vital_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `abnormal` | boolean |  |
| `addedby` | number |  |
| `comments` | string |  |
| `created` | date |  |
| `date_taken` | date |  |
| `encounter_id` | number |  |
| `id` | number |  |
| `object` | string |  |
| `order_id` | number |  |
| `pt_id` | number |  |
| `units` | string |  |
| `url_encounter` | string |  |
| `url_order` | string |  |
| `value` | string |  |
| `vital_id` | number |  |
| `vital_url` | string |  |

## Native endpoint

Through the native Cerbo API, this operation is `GET /patients/:patient_id/vitals/:vital_id` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-patient-custom-vitals.md) for the provider-specific parameters and requirements.

