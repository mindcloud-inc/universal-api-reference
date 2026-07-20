# SafetyCulture: Set Inspection Site

Updates an inspection site in SafetyCulture.

```
PUT https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/set-inspection-site
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SafetyCulture `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/set-inspection-site" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inspectionId": "string",
  "siteId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/set-inspection-site', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inspectionId": "string",
    "siteId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inspectionId` | string | yes | The ID of the inspection |
| `siteId` | string | yes | The ID of the site |

## Response

```json
{
  "success": true,
  "data": [
    {
      "inspectionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `inspectionId` | string |  |

## Native endpoint

Through the native SafetyCulture API, this operation is `PUT /inspections/v1/inspections/{inspection_id}/site` (base URL `https://api.safetyculture.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-inspection-site.md) for the provider-specific parameters and requirements.

