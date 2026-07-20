# ECAL: Bulk Update Events By Reference Type

Updates ECAL events by reference type.

```
PUT https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/bulk-update-events-by-reference-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ECAL `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/bulk-update-events-by-reference-type" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "referenceType": "string",
  "requestBody": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/bulk-update-events-by-reference-type', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "referenceType": "string",
    "requestBody": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `referenceType` | string | yes | Reference type used to bulk update matching events. |
| `requestBody` | object | yes | JSON object matching ECAL's bulk event update payload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "calendarId": "string",
      "id": "string",
      "name": "Ava Chen",
      "reference": "string",
      "referenceType": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calendarId` | string |  |
| `id` | string |  |
| `name` | string |  |
| `reference` | string |  |
| `referenceType` | string |  |
| `status` | string |  |

## Native endpoint

Through the native ECAL API, this operation is `PUT /events/:referenceType` (base URL `https://api.ecal.com/apiv2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-update-events-by-reference-type.md) for the provider-specific parameters and requirements.

