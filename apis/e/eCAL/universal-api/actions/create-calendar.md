# ECAL: Create Calendar

Creates a new calendar in ECAL.

```
POST https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/create-calendar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ECAL `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/create-calendar" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "requestBody": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/create-calendar', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "requestBody": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `requestBody` | object | yes | JSON object matching ECAL's create calendar payload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "genre": "string",
      "id": "string",
      "name": "Ava Chen",
      "publisherId": 1,
      "publisherOrgId": 1,
      "reference": "string",
      "subGenre": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `genre` | string |  |
| `id` | string |  |
| `name` | string |  |
| `publisherId` | number |  |
| `publisherOrgId` | number |  |
| `reference` | string |  |
| `subGenre` | string |  |

## Native endpoint

Through the native ECAL API, this operation is `POST /calendar/` (base URL `https://api.ecal.com/apiv2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-calendar.md) for the provider-specific parameters and requirements.

