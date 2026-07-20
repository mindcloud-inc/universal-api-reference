# Qlik: Export App

Exports an existing app from Qlik.

```
GET https://connect.mindcloud.co/v1/universal/qlik/latest/actions/export-app
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Qlik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qlik/latest/actions/export-app?connectionId=$CONNECTION_ID&appId=65b8f2a1f4b0c2d3e4f56789" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "65b8f2a1f4b0c2d3e4f56789"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qlik/latest/actions/export-app?${params}`, {
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
| `appId` | string | yes | Qlik app ID. Example: `65b8f2a1f4b0c2d3e4f56789`. |
| `noData` | boolean | no | When true, export the app without data. Example: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "href": "string",
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `href` | string |  |
| `id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Qlik API, this operation is `POST /api/v1/apps/:appId/export` (base URL `https://{{credentials.tenantHost}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-app.md) for the provider-specific parameters and requirements.

