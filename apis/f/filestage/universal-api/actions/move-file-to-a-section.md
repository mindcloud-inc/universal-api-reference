# Filestage: Move File to a Section

Moves a Filestage file to a section.

```
PUT https://connect.mindcloud.co/v1/universal/filestage/latest/actions/move-file-to-a-section
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Filestage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/filestage/latest/actions/move-file-to-a-section" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/filestage/latest/actions/move-file-to-a-section', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileId` | string | yes | File Id |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sectionId` | string | no | The ID of the section to move the file into. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "externalId": "string",
      "id": "string",
      "name": "Ava Chen",
      "projectId": "string",
      "reviewLink": "https://example.com",
      "sectionId": "string",
      "versions": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `externalId` | string |  |
| `id` | string |  |
| `name` | string |  |
| `projectId` | string |  |
| `reviewLink` | string |  |
| `sectionId` | string |  |
| `versions` | array<object> |  |

## Native endpoint

Through the native Filestage API, this operation is `PUT /files/{fileId}/section` (base URL `https://api.filestage.io/ext/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-file-to-a-section.md) for the provider-specific parameters and requirements.

