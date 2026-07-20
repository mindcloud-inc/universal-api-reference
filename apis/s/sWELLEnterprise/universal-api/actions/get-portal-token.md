# SWELLEnterprise: Get Portal Token

Retrieves a portal token from SWELLEnterprise.

```
GET https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/get-portal-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SWELLEnterprise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/get-portal-token?connectionId=$CONNECTION_ID&type=string&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "type": "string",
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sWELLEnterprise/latest/actions/get-portal-token?${params}`, {
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
| `type` | string | yes | The type: contact or company. |
| `id` | number | yes | The ID of the contact or company. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expires_at": "2026-05-07T12:00:00.000Z",
      "token": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expires_at` | date |  |
| `token` | string |  |
| `url` | string |  |

## Native endpoint

Through the native SWELLEnterprise API, this operation is `POST /client-portal/token` (base URL `https://dashboard.swellsystem.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-portal-token.md) for the provider-specific parameters and requirements.

