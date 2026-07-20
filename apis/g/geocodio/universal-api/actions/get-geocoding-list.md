# Geocodio: Get Geocoding List

Retrieves geocoding list status from Geocodio.

```
GET https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/get-geocoding-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Geocodio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/get-geocoding-list?connectionId=$CONNECTION_ID&id=42" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "42"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/get-geocoding-list?${params}`, {
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
| `id` | number | yes | Geocodio list ID. Example: `42`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "downloadUrl": "https://example.com",
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "fields": [
        "string"
      ],
      "file": {
        "estimatedRowsCount": 1,
        "filename": "Ava Chen"
      },
      "id": 1,
      "status": {
        "message": "string",
        "progress": 1,
        "state": "string",
        "timeLeftDescription": "string",
        "timeLeftSeconds": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `downloadUrl` | string | Download URL when available. |
| `expiresAt` | date | Result expiration time. |
| `fields` | array<string> | Requested data append fields. |
| `file.estimatedRowsCount` | number | Estimated number of rows. |
| `file.filename` | string | Uploaded filename. |
| `id` | number | List ID. |
| `status.message` | string | Status message. |
| `status.progress` | number | Processing progress percentage. |
| `status.state` | string | Processing state. |
| `status.timeLeftDescription` | string | Estimated time remaining. |
| `status.timeLeftSeconds` | number | Estimated seconds remaining. |

## Native endpoint

Through the native Geocodio API, this operation is `GET /lists/{id}` (base URL `https://api.geocod.io/v1.12`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-geocoding-list.md) for the provider-specific parameters and requirements.

