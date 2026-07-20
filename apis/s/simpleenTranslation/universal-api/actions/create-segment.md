# Simpleen Translation: Create Segment

Creates a new segment in Simpleen Translation.

```
POST https://connect.mindcloud.co/v1/universal/simpleenTranslation/latest/actions/create-segment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simpleen Translation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/simpleenTranslation/latest/actions/create-segment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "source_entry": "string",
  "entry": "string",
  "service": "string",
  "formality": "string",
  "interpolation": "string",
  "source_language": 1,
  "target_language": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simpleenTranslation/latest/actions/create-segment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "source_entry": "string",
    "entry": "string",
    "service": "string",
    "formality": "string",
    "interpolation": "string",
    "source_language": 1,
    "target_language": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `source_entry` | string | yes |  |
| `entry` | string | yes |  |
| `service` | string | yes |  |
| `formality` | string | yes |  |
| `interpolation` | string | yes |  |
| `source_language` | number | yes |  |
| `target_language` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "entry": "string",
      "formality": "string",
      "id": 1,
      "interpolation": "string",
      "path": "string",
      "service": "string",
      "source_entry": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `entry` | string |  |
| `formality` | string |  |
| `id` | number |  |
| `interpolation` | string |  |
| `path` | string |  |
| `service` | string |  |
| `source_entry` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Simpleen Translation API, this operation is `POST /segments` (base URL `https://api.simpleen.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-segment.md) for the provider-specific parameters and requirements.

