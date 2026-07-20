# Wrike: List Space Folders

Finds folders in a Wrike space.

```
GET https://connect.mindcloud.co/v1/universal/wrike/latest/actions/list-space-folders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wrike `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wrike/latest/actions/list-space-folders?connectionId=$CONNECTION_ID&spaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "spaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wrike/latest/actions/list-space-folders?${params}`, {
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
| `spaceId` | string | yes | Wrike space ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "childIds": [
        "string"
      ],
      "color": "string",
      "customItemTypeId": "string",
      "id": "string",
      "project": {},
      "scope": "string",
      "space": true,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `childIds` | array<string> |  |
| `color` | string |  |
| `customItemTypeId` | string |  |
| `id` | string |  |
| `project` | object |  |
| `scope` | string |  |
| `space` | boolean |  |
| `title` | string |  |

## Native endpoint

Through the native Wrike API, this operation is `GET /spaces/:spaceId/folders` (base URL `https://{{credentials.accessTokenRequest.host}}/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-space-folders.md) for the provider-specific parameters and requirements.

