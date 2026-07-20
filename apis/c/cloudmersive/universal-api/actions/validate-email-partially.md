# Cloudmersive: Validate Email Partially

Partially validates an email address in Cloudmersive.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/validate-email-partially
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/validate-email-partially?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/validate-email-partially?${params}`, {
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
| `email` | string | no | Email address to check against mail servers. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "servers": [
        "string"
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `servers` | array<string> |  |
| `success` | boolean |  |

## Native endpoint

Through the native Cloudmersive API, this operation is `POST /validate/email/address/servers` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-email-partially.md) for the provider-specific parameters and requirements.

