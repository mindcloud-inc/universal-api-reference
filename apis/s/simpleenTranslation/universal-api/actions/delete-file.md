# Simpleen Translation: Delete File

Deletes an existing file from Simpleen Translation.

```
DELETE https://connect.mindcloud.co/v1/universal/simpleenTranslation/latest/actions/delete-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simpleen Translation `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/simpleenTranslation/latest/actions/delete-file?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpleenTranslation/latest/actions/delete-file?${params}`, {
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
| `id` | number | yes |  |

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

Through the native Simpleen Translation API, this operation is `DELETE /files/:id` (base URL `https://api.simpleen.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-file.md) for the provider-specific parameters and requirements.

