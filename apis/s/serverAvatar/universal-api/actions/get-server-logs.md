# ServerAvatar: Get Server Logs

Retrieves server logs from ServerAvatar.

```
GET https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/get-server-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServerAvatar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/get-server-logs?connectionId=$CONNECTION_ID&organization=string&server=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organization": "string",
  "server": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/get-server-logs?${params}`, {
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
| `organization` | string | yes |  |
| `server` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "logFiles": {
        "auth": {
          "log": "string"
        },
        "kern": {
          "log": "string"
        },
        "letsencrypt": {
          "log": "string"
        },
        "mail": {
          "log": "string"
        },
        "mysql/error": {
          "log": "string"
        },
        "nginx/access": {
          "log": "string"
        },
        "nginx/error": {
          "log": "string"
        },
        "php7": {
          "0-fpm": {
            "log": "string"
          },
          "1-fpm": {
            "log": "string"
          },
          "2-fpm": {
            "log": "string"
          },
          "3-fpm": {
            "log": "string"
          },
          "4-fpm": {
            "log": "string"
          }
        },
        "php8": {
          "0-fpm": {
            "log": "string"
          },
          "1-fpm": {
            "log": "string"
          },
          "2-fpm": {
            "log": "string"
          }
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `logFiles` | object |  |
| `logFiles.auth.log` | string |  |
| `logFiles.kern.log` | string |  |
| `logFiles.letsencrypt.log` | string |  |
| `logFiles.mail.log` | string |  |
| `logFiles.mysql/error.log` | string |  |
| `logFiles.nginx/access.log` | string |  |
| `logFiles.nginx/error.log` | string |  |
| `logFiles.php7.0-fpm.log` | string |  |
| `logFiles.php7.1-fpm.log` | string |  |
| `logFiles.php7.2-fpm.log` | string |  |
| `logFiles.php7.3-fpm.log` | string |  |
| `logFiles.php7.4-fpm.log` | string |  |
| `logFiles.php8.0-fpm.log` | string |  |
| `logFiles.php8.1-fpm.log` | string |  |
| `logFiles.php8.2-fpm.log` | string |  |

## Native endpoint

Through the native ServerAvatar API, this operation is `GET /organizations/{{organization}}/servers/{{server}}/logs` (base URL `https://api.serveravatar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-server-logs.md) for the provider-specific parameters and requirements.

