# AirPinpoint: Generate Share Link

Creates a temporary share link for a trackable in AirPinpoint.

```
POST https://connect.mindcloud.co/v1/universal/airPinpoint/latest/actions/generate-share-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AirPinpoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/airPinpoint/latest/actions/generate-share-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "hours": 1,
  "trackableId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/airPinpoint/latest/actions/generate-share-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "hours": 1,
    "trackableId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `hours` | number | yes |  |
| `trackableId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "shareUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `shareUrl` | string | Temporary AirPinpoint share URL for the requested trackable. |

## Native endpoint

Through the native AirPinpoint API, this operation is `POST /share-links` (base URL `https://api.airpinpoint.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-share-link.md) for the provider-specific parameters and requirements.

