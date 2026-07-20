# ServerAvatar: Get Application Log Sizes

Retrieves application log sizes from ServerAvatar.

```
GET https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/get-application-log-sizes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServerAvatar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/get-application-log-sizes?connectionId=$CONNECTION_ID&organization=string&server=string&application=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organization": "string",
  "server": "string",
  "application": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/get-application-log-sizes?${params}`, {
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
| `application` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "output": {
        "access-ssl": {
          "log": {
            "size": "string",
            "title": "string"
          }
        },
        "access": {
          "log": {
            "size": "string",
            "title": "string"
          }
        },
        "error-ssl": {
          "log": {
            "size": "string",
            "title": "string"
          }
        },
        "error": {
          "log": {
            "size": "string",
            "title": "string"
          }
        }
      },
      "sizeType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `output` | object |  |
| `output.access-ssl.log` | object |  |
| `output.access-ssl.log.size` | string |  |
| `output.access-ssl.log.title` | string |  |
| `output.access.log` | object |  |
| `output.access.log.size` | string |  |
| `output.access.log.title` | string |  |
| `output.error-ssl.log` | object |  |
| `output.error-ssl.log.size` | string |  |
| `output.error-ssl.log.title` | string |  |
| `output.error.log` | object |  |
| `output.error.log.size` | string |  |
| `output.error.log.title` | string |  |
| `sizeType` | string |  |

## Native endpoint

Through the native ServerAvatar API, this operation is `GET /organizations/{{organization}}/servers/{{server}}/applications/{{application}}/log-sizes` (base URL `https://api.serveravatar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-application-log-sizes.md) for the provider-specific parameters and requirements.

