# EndBounce: Find Email

Finds an email in EndBounce by name and domain.

```
GET https://connect.mindcloud.co/v1/universal/endBounce/latest/actions/find-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EndBounce `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/endBounce/latest/actions/find-email?connectionId=$CONNECTION_ID&name=Ava%20Chen&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen",
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/endBounce/latest/actions/find-email?${params}`, {
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
| `name` | string | yes | Full name to search for. |
| `domain` | string | yes | Company domain to search against. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "found": true,
      "message": "string",
      "method": "string",
      "requestId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Discovered email address when one is found. |
| `found` | boolean | Whether an email was found. |
| `message` | string | Provider message describing the lookup result. |
| `method` | string | Method used to find the email. |
| `requestId` | string | Finder request ID. |
| `status` | string | Finder status. |

## Native endpoint

Through the native EndBounce API, this operation is `POST /v1/finder` (base URL `https://api.endbounce.com/api/integrations`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-email.md) for the provider-specific parameters and requirements.

