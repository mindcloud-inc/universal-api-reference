# Aspire: Refresh Authorization Token

Refreshes the current authorization token in Aspire.

```
GET https://connect.mindcloud.co/v1/universal/aspire/latest/actions/refresh-authorization-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/refresh-authorization-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspire/latest/actions/refresh-authorization-token?${params}`, {
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
| `refreshToken` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "RefreshToken": "string",
      "Token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `RefreshToken` | string |  |
| `Token` | string |  |

## Native endpoint

Through the native Aspire API, this operation is `POST Authorization/RefreshToken` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/refresh-authorization-token.md) for the provider-specific parameters and requirements.

