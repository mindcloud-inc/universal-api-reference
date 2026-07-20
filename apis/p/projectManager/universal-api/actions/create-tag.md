# ProjectManager: Create Tag

Creates a new tag in ProjectManager.

```
POST https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/create-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProjectManager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/create-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "MindCloud Sample"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/create-tag', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "MindCloud Sample"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The name of this Tag. Example: `MindCloud Sample`. |
| `color` | string | no | The color that will be used to represent this Tag visually. This color is automatically chosen by the application when a user creates a Tag. You can choose specify any color that can be represented using HTML RGB syntax such as `#0088FF`, in the format `RRGGBB`. You may not use names for colors. Example: `#336699`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native ProjectManager API, this operation is `POST /api/data/tags` (base URL `https://api.projectmanager.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tag.md) for the provider-specific parameters and requirements.

