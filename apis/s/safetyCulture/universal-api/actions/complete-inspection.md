# SafetyCulture: Complete Inspection

Completes an inspection in SafetyCulture.

```
PUT https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/complete-inspection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SafetyCulture `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/complete-inspection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inspectionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/complete-inspection', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inspectionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inspectionId` | string | yes | The unique identifier for the inspection to complete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "inspectionIdentity": {
        "inspectionId": "string",
        "organisationId": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `inspectionIdentity.inspectionId` | string |  |
| `inspectionIdentity.organisationId` | string |  |

## Native endpoint

Through the native SafetyCulture API, this operation is `POST /inspections/integration/v1/inspections/{inspection_id}/complete` (base URL `https://api.safetyculture.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/complete-inspection.md) for the provider-specific parameters and requirements.

