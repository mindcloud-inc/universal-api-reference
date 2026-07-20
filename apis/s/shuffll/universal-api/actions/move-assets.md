# Shuffll: Move Assets

Updates asset locations in Shuffll.

```
PUT https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/move-assets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shuffll `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/move-assets" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "assetIds[]": [
    "string"
  ],
  "organizationId": "69cac8104c4a701fd26271a1",
  "toFolder": "string",
  "workspaceId": "69cac8104c4a701fd26271a5"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shuffll/latest/actions/move-assets', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "assetIds[]": ["string"],
    "organizationId": "69cac8104c4a701fd26271a1",
    "toFolder": "string",
    "workspaceId": "69cac8104c4a701fd26271a5"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assetIds[]` | array<string> | yes | Asset ids to move. |
| `organizationId` | string | yes | Shuffll organization id. Default: `69cac8104c4a701fd26271a1`. |
| `toFolder` | string | yes | Destination folder name. |
| `workspaceId` | string | yes | Shuffll workspace id. Default: `69cac8104c4a701fd26271a5`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the assets were moved. |

## Native endpoint

Through the native Shuffll API, this operation is `PUT /auth/organization/:organizationId/workspace/:workspaceId/assets/move` (base URL `https://api.shuffll.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-assets.md) for the provider-specific parameters and requirements.

