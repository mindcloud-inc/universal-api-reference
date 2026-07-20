# Dash.app: Get Asset Files

Retrieves files for an asset from Dash.app.

```
GET https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/get-asset-files
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dash.app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/get-asset-files?connectionId=$CONNECTION_ID&id=7af90a8b-7ccd-430f-a85d-e8614015bc47" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "7af90a8b-7ccd-430f-a85d-e8614015bc47"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/get-asset-files?${params}`, {
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
| `id` | string | yes | Example: `7af90a8b-7ccd-430f-a85d-e8614015bc47`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results` | array<object> |  |

## Native endpoint

Through the native Dash.app API, this operation is `GET /assets/:id/files` (base URL `https://api-v2.dash.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-asset-files.md) for the provider-specific parameters and requirements.

