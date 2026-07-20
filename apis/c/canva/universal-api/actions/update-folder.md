# Canva: Update Folder

Updates an existing folder in Canva.

```
PUT https://connect.mindcloud.co/v1/universal/canva/latest/actions/update-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Canva `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/canva/latest/actions/update-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "folderId": "FAHDrkEuHo0",
  "name": "MC Stage3 Source Folder 2203 Updated"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/canva/latest/actions/update-folder', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "folderId": "FAHDrkEuHo0",
    "name": "MC Stage3 Source Folder 2203 Updated"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `folderId` | string | yes | Example: `FAHDrkEuHo0`. |
| `name` | string | yes | Example: `MC Stage3 Source Folder 2203 Updated`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "folder": {
        "createdAt": 1,
        "id": "string",
        "name": "Ava Chen",
        "updatedAt": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `folder` | object |  |
| `folder.createdAt` | number |  |
| `folder.id` | string |  |
| `folder.name` | string |  |
| `folder.updatedAt` | number |  |

## Native endpoint

Through the native Canva API, this operation is `PATCH /v1/folders/:folderId` (base URL `https://api.canva.com/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-folder.md) for the provider-specific parameters and requirements.

