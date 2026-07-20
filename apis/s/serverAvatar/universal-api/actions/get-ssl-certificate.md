# ServerAvatar: Get SSL Certificate

Retrieves an SSL certificate from ServerAvatar.

```
GET https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/get-ssl-certificate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServerAvatar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/get-ssl-certificate?connectionId=$CONNECTION_ID&organization=string&server=string&application=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organization": "string",
  "server": "string",
  "application": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/get-ssl-certificate?${params}`, {
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
      "certificateInfo": {
        "domains": [
          "string"
        ],
        "expiresOn": "string",
        "isExpired": true,
        "issuedOn": "string",
        "issuer": "string",
        "primaryDomain": "string",
        "tempDomain": 1,
        "type": "string",
        "validityLeft": 1
      },
      "forceHttps": 1,
      "installed": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `certificateInfo` | object |  |
| `certificateInfo.domains` | array<string> |  |
| `certificateInfo.expiresOn` | string |  |
| `certificateInfo.isExpired` | boolean |  |
| `certificateInfo.issuedOn` | string |  |
| `certificateInfo.issuer` | string |  |
| `certificateInfo.primaryDomain` | string |  |
| `certificateInfo.tempDomain` | number |  |
| `certificateInfo.type` | string |  |
| `certificateInfo.validityLeft` | number |  |
| `forceHttps` | number |  |
| `installed` | boolean |  |

## Native endpoint

Through the native ServerAvatar API, this operation is `GET /organizations/{{organization}}/servers/{{server}}/applications/{{application}}/ssl` (base URL `https://api.serveravatar.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ssl-certificate.md) for the provider-specific parameters and requirements.

