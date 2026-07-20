# 24 Pull Requests: Get Organisation

Retrieves an organisation from 24 Pull Requests.

```
GET https://connect.mindcloud.co/v1/universal/pullRequests/latest/actions/get-organisation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 24 Pull Requests `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pullRequests/latest/actions/get-organisation?connectionId=$CONNECTION_ID&login=uswitch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "login": "uswitch"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pullRequests/latest/actions/get-organisation?${params}`, {
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
| `login` | string | yes | Organisation login from the 24 Pull Requests organisation URL. Example: `uswitch`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatar_url": "https://example.com",
      "link": "https://example.com",
      "login": "string",
      "users": [
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
| `avatar_url` | string | Organisation avatar URL. |
| `link` | string | Organisation page URL. |
| `login` | string | Organisation login. |
| `users` | array<object> | Organisation users. |

## Native endpoint

Through the native 24 Pull Requests API, this operation is `GET /organisations/:login.json` (base URL `https://24pullrequests.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organisation.md) for the provider-specific parameters and requirements.

