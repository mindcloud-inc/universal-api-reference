# Otiom: List Geofences

Retrieves geofences from Otiom.

```
GET https://connect.mindcloud.co/v1/universal/otiom/latest/actions/list-geofences
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Otiom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/otiom/latest/actions/list-geofences?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/otiom/latest/actions/list-geofences?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Otiom API, this operation is `GET /api/geofences/` (base URL `https://api.otiom.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-geofences.md) for the provider-specific parameters and requirements.

