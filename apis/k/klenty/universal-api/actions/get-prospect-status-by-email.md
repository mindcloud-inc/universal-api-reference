# Klenty: Get Prospect Status By Email

Retrieves prospect status from Klenty by email.

```
GET https://connect.mindcloud.co/v1/universal/klenty/latest/actions/get-prospect-status-by-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Klenty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/klenty/latest/actions/get-prospect-status-by-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/klenty/latest/actions/get-prospect-status-by-email?${params}`, {
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
| `email` | string | yes | Prospect email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cadenceStatus": "string",
      "prospectStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cadenceStatus` | string |  |
| `prospectStatus` | string |  |

## Native endpoint

Through the native Klenty API, this operation is `GET /prospects/{{email}}/status` (base URL `https://api.klenty.com/apis/v1/user/{{credentials.username}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-prospect-status-by-email.md) for the provider-specific parameters and requirements.

