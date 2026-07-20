# Dash.app: Create Asset Share

Creates a new asset share in Dash.app.

```
POST https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/create-asset-share
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dash.app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/create-asset-share" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "assetIds[]": "7af90a8b-7ccd-430f-a85d-e8614015bc47",
  "expiry": "null"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/create-asset-share', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "assetIds[]": "7af90a8b-7ccd-430f-a85d-e8614015bc47",
    "expiry": "null"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assetIds[]` | array<string> | yes | Example: `7af90a8b-7ccd-430f-a85d-e8614015bc47`. |
| `assetPermittedActions` | string | no | Default: `VIEW`. Example: `VIEW`. |
| `expiry` | string | yes | Default: `null`. Example: `null`. |

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

Through the native Dash.app API, this operation is `POST /asset-shares` (base URL `https://api-v2.dash.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-asset-share.md) for the provider-specific parameters and requirements.

