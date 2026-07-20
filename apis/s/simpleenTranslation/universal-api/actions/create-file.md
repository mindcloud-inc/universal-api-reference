# Simpleen Translation: Create File

Creates a new file in Simpleen Translation.

```
POST https://connect.mindcloud.co/v1/universal/simpleenTranslation/latest/actions/create-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simpleen Translation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/simpleenTranslation/latest/actions/create-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "dataformat": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simpleenTranslation/latest/actions/create-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "dataformat": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `dataformat` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cntSegments": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "dataformat": "string",
      "filepath": "string",
      "formality": "string",
      "id": 1,
      "interpolation": "string",
      "name": "Ava Chen",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cntSegments` | number |  |
| `created_at` | date |  |
| `dataformat` | string |  |
| `filepath` | string |  |
| `formality` | string |  |
| `id` | number |  |
| `interpolation` | string |  |
| `name` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Simpleen Translation API, this operation is `POST /files` (base URL `https://api.simpleen.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-file.md) for the provider-specific parameters and requirements.

