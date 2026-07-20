# Cerbo: List Patient Height Vitals

Retrieves patient height vitals from Cerbo.

```
GET https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-patient-height-vitals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-patient-height-vitals?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-patient-height-vitals?${params}`, {
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
| `patient_id` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addedby": 1,
      "comments": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "date_taken": "2026-05-07T12:00:00.000Z",
      "height": 1,
      "id": 1,
      "object": "string",
      "pt_id": 1,
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
| `comments` | string |  |
| `created` | date |  |
| `date_taken` | date |  |
| `height` | number |  |
| `id` | number |  |
| `object` | string |  |
| `pt_id` | number |  |
| `units` | string |  |

## Native endpoint

Through the native Cerbo API, this operation is `GET /patients/:patient_id/vitals/height` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-patient-height-vitals.md) for the provider-specific parameters and requirements.

