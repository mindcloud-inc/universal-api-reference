# Recreation.gov: Update Rec Area

Updates an existing recreation area in Recreation.gov.

```
PUT https://connect.mindcloud.co/v1/universal/recreationgov/latest/actions/update-rec-area
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recreation.gov `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/recreationgov/latest/actions/update-rec-area" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "name": "Ava Chen",
  "description": "string",
  "directions": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recreationgov/latest/actions/update-rec-area', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "name": "Ava Chen",
    "description": "string",
    "directions": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes |  |
| `orgId` | number | no |  |
| `orgRefId` | string | no |  |
| `name` | string | yes |  |
| `description` | string | yes |  |
| `feeDescription` | string | no |  |
| `directions` | string | yes |  |
| `accessibilityText` | string | no |  |
| `phone` | string | no |  |
| `email` | string | no |  |
| `reservationUrl` | string | no |  |
| `mapUrl` | string | no |  |
| `longitude` | number | no |  |
| `latitude` | number | no |  |
| `stayLimit` | string | no |  |
| `enabled` | boolean | no |  |
| `reservable` | boolean | no |  |
| `keywords` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "MESSAGE": "string",
      "STATUSCODE": 1,
      "SUCCESS": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `MESSAGE` | string |  |
| `STATUSCODE` | number |  |
| `SUCCESS` | boolean |  |

## Native endpoint

Through the native Recreation.gov API, this operation is `PUT /recareas/{id}` (base URL `https://ridb.recreation.gov/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-rec-area.md) for the provider-specific parameters and requirements.

