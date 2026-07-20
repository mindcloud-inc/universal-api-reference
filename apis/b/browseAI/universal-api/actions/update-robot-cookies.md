# Browse AI: Update Robot Cookies

Updates robot cookies in Browse AI.

```
PUT https://connect.mindcloud.co/v1/universal/browseAI/latest/actions/update-robot-cookies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Browse AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/browseAI/latest/actions/update-robot-cookies" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "robotId": "c3689adb-50aa-44af-b265-a7e0d4e5846e",
  "cookies[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/browseAI/latest/actions/update-robot-cookies', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "robotId": "c3689adb-50aa-44af-b265-a7e0d4e5846e",
    "cookies[]": [{}],
    "cookies[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `robotId` | string | yes | Unique robot ID You can find a robot's ID by opening it on the dashboard and copying its ID in the browser address bar. Example: `c3689adb-50aa-44af-b265-a7e0d4e5846e`. |
| `cookies[]` | array<object> | yes | Array of cookies to store on the robot. |
| `cookies[]` | array<object> | yes | Array of cookies to store on the robot. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "domain": "string",
      "expirationDate": 1,
      "hostOnly": true,
      "httpOnly": true,
      "name": "Ava Chen",
      "path": "string",
      "secure": true,
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domain` | string | The domain associated with the cookie. Specifies the domains to which the cookie should be sent. |
| `expirationDate` | number | The expiration date of the cookie in seconds since the UNIX epoch (e.g., POSIX time). If not provided, the cookie will be treated as a session cookie. |
| `hostOnly` | boolean | If true, the cookie is only sent to the exact domain specified in the "domain" property. If false, the cookie is sent to subdomains as well, provided that the "domain" property allows it. |
| `httpOnly` | boolean | If true, the cookie is accessible only through the HTTP(S) protocol and cannot be accessed through JavaScript or other client-side scripts. |
| `name` | string | The name of the cookie. |
| `path` | string | The URL path to which the cookie should be sent. If not provided, it defaults to the current path of the document location. |
| `secure` | boolean | Indicates whether the cookie should only be sent over secure (HTTPS) connections. If true, the cookie will not be sent over unencrypted HTTP connections. |
| `value` | string | The value of the cookie. |

## Native endpoint

Through the native Browse AI API, this operation is `PATCH /robots/:robotId/cookies` (base URL `https://api.browse.ai/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-robot-cookies.md) for the provider-specific parameters and requirements.

