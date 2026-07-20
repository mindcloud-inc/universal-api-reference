# Otiom: Get Geofence

Retrieves a geofence from Otiom.

```
GET https://connect.mindcloud.co/v1/universal/otiom/latest/actions/get-geofence
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Otiom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/otiom/latest/actions/get-geofence?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/otiom/latest/actions/get-geofence?${params}`, {
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
| `id` | number | yes | A unique integer value identifying this geo fence. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "administrating": true,
      "id": 1,
      "name": "Ava Chen",
      "patient": 1,
      "patients": [
        1
      ],
      "points": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `administrating` | boolean |  |
| `id` | number |  |
| `name` | string |  |
| `patient` | number |  |
| `patients` | array<number> |  |
| `points` | array<array> |  |

## Native endpoint

Through the native Otiom API, this operation is `GET /api/geofences/:id/` (base URL `https://api.otiom.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-geofence.md) for the provider-specific parameters and requirements.

