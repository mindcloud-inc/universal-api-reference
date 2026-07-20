# Sendible: Rename Media Library



```
PUT https://connect.mindcloud.co/v1/universal/sendible/latest/actions/rename-media-library
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendible `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sendible/latest/actions/rename-media-library" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mediaLibraryId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendible/latest/actions/rename-media-library', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mediaLibraryId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mediaLibraryId` | string | yes | The media library ID to rename. |
| `name` | string | yes | New media library name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `name` | string |  |

## Native endpoint

Through the native Sendible API, this operation is `PUT 0.1/tw/media_libraries` (base URL `https://api.sendible.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rename-media-library.md) for the provider-specific parameters and requirements.

