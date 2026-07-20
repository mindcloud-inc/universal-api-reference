# Pabbly Hook: Move Connection To Folder



```
PUT https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/move-connection-to-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Hook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/move-connection-to-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "connectionIds[]": "conn_4d2890e85bc340b3be31406456a1a7a6",
  "fromFolderId": "664ef7516cf2e1f425971214",
  "toFolderId": "664edfc3b2be40a4309362be"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/move-connection-to-folder', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "connectionIds[]": "conn_4d2890e85bc340b3be31406456a1a7a6",
    "fromFolderId": "664ef7516cf2e1f425971214",
    "toFolderId": "664edfc3b2be40a4309362be"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `connectionIds[]` | array<string> | yes | Connection IDs to move. Example: `conn_4d2890e85bc340b3be31406456a1a7a6`. |
| `fromFolderId` | string | yes | Current folder ID. Example: `664ef7516cf2e1f425971214`. |
| `toFolderId` | string | yes | Destination folder ID. Example: `664edfc3b2be40a4309362be`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Pabbly Hook connection move confirmation message. |

## Native endpoint

Through the native Pabbly Hook API, this operation is `PUT /api/v1/folders/move-connection` (base URL `https://hook.pabbly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-connection-to-folder.md) for the provider-specific parameters and requirements.

