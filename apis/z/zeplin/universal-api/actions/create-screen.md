# Zeplin: Create Screen

Creates a new screen in Zeplin.

```
POST https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/create-screen
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeplin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/create-screen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "name": "Ava Chen",
  "image": "string",
  "description": "string",
  "commitMessage": "string",
  "commitColor": "string",
  "tags[]": [
    "string"
  ],
  "sectionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/create-screen', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "name": "Ava Chen",
    "image": "string",
    "description": "string",
    "commitMessage": "string",
    "commitColor": "string",
    "tags[]": ["string"],
    "sectionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | Project id |
| `name` | string | yes | Name of the screen |
| `image` | file | yes | Binary data of the screen image. The image has to be in JPEG or PNG format, and its size cannot exceed 5MB. |
| `description` | string | yes | Description for the screen |
| `commitMessage` | string | yes | Commit message for the screen version |
| `commitColor` | string | yes | Commit color for the screen version |
| `tags[]` | array<string> | yes | Tags for the screen |
| `sectionId` | string | yes | Unique id of the screen section |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Zeplin API, this operation is `POST /projects/{project_id}/screens` (base URL `https://api.zeplin.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-screen.md) for the provider-specific parameters and requirements.

