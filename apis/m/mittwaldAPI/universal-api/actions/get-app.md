# mittwald: Get App

Retrieves app from mittwald API.

```
GET https://connect.mindcloud.co/v1/universal/mittwaldAPI/latest/actions/get-app
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a mittwald `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mittwaldAPI/latest/actions/get-app?connectionId=$CONNECTION_ID&appId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mittwaldAPI/latest/actions/get-app?${params}`, {
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
| `appId` | string | yes | The app ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actionCapabilities": [
        "string"
      ],
      "id": "string",
      "name": "Ava Chen",
      "tags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionCapabilities` | array<string> |  |
| `id` | string |  |
| `name` | string |  |
| `tags` | array<string> |  |

## Native endpoint

Through the native mittwald API, this operation is `GET /v2/apps/:appId` (base URL `https://api.mittwald.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-app.md) for the provider-specific parameters and requirements.

