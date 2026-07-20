# Dash.app: Update Asset Share

Updates an existing asset share in Dash.app.

```
PUT https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/update-asset-share
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dash.app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/update-asset-share" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "df615fba-14b9-4d29-b4a9-43fff17b1ad0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/update-asset-share', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "df615fba-14b9-4d29-b4a9-43fff17b1ad0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assetPermittedActions` | string | no | Default: `VIEW_AND_DOWNLOAD`. Example: `VIEW_AND_DOWNLOAD`. |
| `expiry` | string | no | Example: `[object Object]`. |
| `id` | string | yes | Default: `df615fba-14b9-4d29-b4a9-43fff17b1ad0`. Example: `df615fba-14b9-4d29-b4a9-43fff17b1ad0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "permittedActions": [
        {}
      ],
      "result": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `permittedActions` | array<object> |  |
| `result` | object |  |

## Native endpoint

Through the native Dash.app API, this operation is `PATCH /asset-shares/:id` (base URL `https://api-v2.dash.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-asset-share.md) for the provider-specific parameters and requirements.

