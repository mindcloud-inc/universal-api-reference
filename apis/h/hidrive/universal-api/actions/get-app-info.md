# HiDrive: Get App Info

Retrieves app information from HiDrive.

```
GET https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/get-app-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HiDrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/get-app-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/get-app-info?${params}`, {
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
| `fields` | string | no | Comma-separated app information fields to include. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": 1,
      "developer": {},
      "homepage": "string",
      "id": 1,
      "name": "Ava Chen",
      "refresh_token": {
        "scope": "string"
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | number | Application creation timestamp. |
| `developer` | object | Developer metadata for the application. |
| `homepage` | string | Application homepage URL. |
| `id` | number | HiDrive application identifier. |
| `name` | string | Application name. |
| `refresh_token` | object | Refresh-token configuration metadata. |
| `refresh_token.scope` | string | Configured refresh-token scope string. |
| `status` | string | Application status. |

## Native endpoint

Through the native HiDrive API, this operation is `GET /app/me` (base URL `https://api.hidrive.strato.com/2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-app-info.md) for the provider-specific parameters and requirements.

