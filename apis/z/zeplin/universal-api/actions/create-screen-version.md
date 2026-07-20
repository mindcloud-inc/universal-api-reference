# Zeplin: Create Screen Version

Creates a new screen version in Zeplin.

```
POST https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/create-screen-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zeplin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/create-screen-version" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "screenId": "string",
  "image": "string",
  "commitMessage": "string",
  "commitColor": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zeplin/latest/actions/create-screen-version', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "screenId": "string",
    "image": "string",
    "commitMessage": "string",
    "commitColor": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | Project id |
| `screenId` | string | yes | Screen id |
| `image` | file | yes | Binary data of the screen image. The image has to be in JPEG or PNG format, and its size cannot exceed 5MB. |
| `commitMessage` | string | yes | Commit message for the screen version |
| `commitColor` | string | yes | Commit color for the screen version |

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

Through the native Zeplin API, this operation is `POST /projects/{project_id}/screens/{screen_id}/versions` (base URL `https://api.zeplin.dev/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-screen-version.md) for the provider-specific parameters and requirements.

