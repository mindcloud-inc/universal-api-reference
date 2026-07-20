# Invision Community: Get Cloud Login Handler Member



```
GET https://connect.mindcloud.co/v1/universal/invisionCommunity/latest/actions/get-cloud-login-handler-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invision Community `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invisionCommunity/latest/actions/get-cloud-login-handler-member?connectionId=$CONNECTION_ID&handler_id=string&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "handler_id": "string",
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invisionCommunity/latest/actions/get-cloud-login-handler-member?${params}`, {
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
| `handler_id` | string | yes | Login handler identifier. |
| `id` | number | yes | Member identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "profileUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `profileUrl` | string |  |

## Native endpoint

Through the native Invision Community API, this operation is `GET /cloud/loginhandlers/:handler_id/member/:id` (base URL `{{credentials.communityBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-cloud-login-handler-member.md) for the provider-specific parameters and requirements.

