# Geocodio: Create Geocoding List

Creates a new geocoding list in Geocodio.

```
POST https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/create-geocoding-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Geocodio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/create-geocoding-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "direction": "0",
  "format": "{{A}} {{B}}, {{C}} {{D}}"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/create-geocoding-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "direction": "0",
    "format": "{{A}} {{B}}, {{C}} {{D}}"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | no | CSV, TSV, Excel, or ZIP file to upload. |
| `direction` | string | yes | Whether to forward geocode addresses or reverse geocode coordinates. One of: `0`, `1`. |
| `format` | string | yes | Column format template, such as {{A}} {{B}}, {{C}} {{D}}. Example: `{{A}} {{B}}, {{C}} {{D}}`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields` | string | no | Optional data append fields for geocoding list results. Accepts multiple values in one string, delimited by `,`. Example: `timezone,cd`. |
| `callback` | string | no | Optional callback URL for completion notification. Example: `https://example.com/webhook/geocodio-list-complete`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "file": {
        "estimatedRowsCount": 1,
        "filename": "Ava Chen",
        "headers": [
          "string"
        ]
      },
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `file` | object | Uploaded file metadata. |
| `file.estimatedRowsCount` | number | Estimated number of data rows. |
| `file.filename` | string | Uploaded filename. |
| `file.headers` | array<string> | Column headers from the uploaded file. |
| `id` | number | List ID. |

## Native endpoint

Through the native Geocodio API, this operation is `POST /lists` (base URL `https://api.geocod.io/v1.12`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-geocoding-list.md) for the provider-specific parameters and requirements.

