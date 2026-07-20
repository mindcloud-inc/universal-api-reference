# Otiom: List Tracks

Retrieves tracks from Otiom.

```
GET https://connect.mindcloud.co/v1/universal/otiom/latest/actions/list-tracks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Otiom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/otiom/latest/actions/list-tracks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/otiom/latest/actions/list-tracks?${params}`, {
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
      "id": 1,
      "otiom_tag": {
        "id": 1,
        "mac_address": "string",
        "name": "Ava Chen"
      },
      "patient": 1,
      "points": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `otiom_tag.id` | number |  |
| `otiom_tag.mac_address` | string |  |
| `otiom_tag.name` | string |  |
| `patient` | number |  |
| `points` | array |  |

## Native endpoint

Through the native Otiom API, this operation is `GET /api/track/` (base URL `https://api.otiom.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tracks.md) for the provider-specific parameters and requirements.

