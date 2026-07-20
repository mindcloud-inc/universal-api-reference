# Viewneo: Create Folder

Creates a new media folder in Viewneo.

```
POST https://connect.mindcloud.co/v1/universal/viewneo/latest/actions/create-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viewneo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/viewneo/latest/actions/create-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mediaFileIdAsParentDirectory": 1,
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viewneo/latest/actions/create-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mediaFileIdAsParentDirectory": 1,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mediaFileIdAsParentDirectory` | number | yes | ID of folder |
| `name` | string | yes | Name of directory |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyId": 1,
      "createdAt": "string",
      "id": 1,
      "isDefault": true,
      "isShared": true,
      "mediaFileIdAsParentDirectory": {},
      "name": "Ava Chen",
      "type": 1,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyId` | number |  |
| `createdAt` | string |  |
| `id` | number |  |
| `isDefault` | boolean |  |
| `isShared` | boolean |  |
| `mediaFileIdAsParentDirectory` | object |  |
| `name` | string |  |
| `type` | number |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Viewneo API, this operation is `POST /mediafile` (base URL `https://cloud.viewneo.com/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-folder.md) for the provider-specific parameters and requirements.

