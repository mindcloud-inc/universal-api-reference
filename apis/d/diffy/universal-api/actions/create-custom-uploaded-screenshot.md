# Diffy: Create Custom Uploaded Screenshot

Creates a custom uploaded screenshot in Diffy.

```
POST https://connect.mindcloud.co/v1/universal/diffy/latest/actions/create-custom-uploaded-screenshot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Diffy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/diffy/latest/actions/create-custom-uploaded-screenshot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "snapshotName": "Ava Chen",
  "files": "string",
  "urls[]": [
    "https://example.com"
  ],
  "breakpoints[]": [
    1
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/diffy/latest/actions/create-custom-uploaded-screenshot', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "snapshotName": "Ava Chen",
    "files": "string",
    "urls[]": ["https://example.com"],
    "breakpoints[]": [1]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Project ID. |
| `snapshotName` | string | yes | Screenshot name |
| `files` | file | yes | Image file to upload as the custom snapshot. |
| `urls[]` | array<string> | yes | URLs for uploaded screenshot items |
| `breakpoints[]` | array<number> | yes | Breakpoints for uploaded screenshot items |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Created screenshot identifier. |

## Native endpoint

Through the native Diffy API, this operation is `POST /projects/:id/create-custom-snapshot` (base URL `https://app.diffy.website/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-custom-uploaded-screenshot.md) for the provider-specific parameters and requirements.

