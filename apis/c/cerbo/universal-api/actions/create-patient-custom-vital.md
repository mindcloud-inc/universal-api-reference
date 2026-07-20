# Cerbo: Create Patient Custom Vital

Creates a new patient custom vital in Cerbo.

```
POST https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/create-patient-custom-vital
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/create-patient-custom-vital" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/create-patient-custom-vital', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `patient_id` | number | no |  |
| `vital_id` | number | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `value` | string | no |  |
| `abnormal` | boolean | no | A boolean value to indicate if the reading should be marked as abnormal. If left blank, defaults to false (the vital reading is added as “normal”) |
| `comments` | string | no |  |
| `date_taken` | string | no | A string specifying the date and time of the vital reading (if no valid 3-letter timezone specified, defaults to UTC). If left blank, defaults to the current time. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cerbo API returns.

## Native endpoint

Through the native Cerbo API, this operation is `POST /patients/:patient_id/vitals/:vital_id` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-patient-custom-vital.md) for the provider-specific parameters and requirements.

