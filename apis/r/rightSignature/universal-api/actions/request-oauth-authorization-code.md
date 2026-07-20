# RightSignature: Request OAuth Authorization Code

Requests a RightSignature OAuth authorization code.

```
GET https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/request-oauth-authorization-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RightSignature `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/request-oauth-authorization-code?connectionId=$CONNECTION_ID&clientId=string&redirectUri=string&responseType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "clientId": "string",
  "redirectUri": "string",
  "responseType": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rightSignature/latest/actions/request-oauth-authorization-code?${params}`, {
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
| `clientId` | string | yes | The API Key's Client ID |
| `redirectUri` | string | yes | Where the user-agent will be redirected to after an authorization code is granted. Note that this MUST match what is on record with the API Key associated with the passed in client id |
| `responseType` | string | yes | Requests the authorization code grant |
| `scope` | string | no | Level of access that the application is requesting. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |

## Native endpoint

Through the native RightSignature API, this operation is `GET https://api.rightsignature.com/oauth/authorize` (base URL `https://api.rightsignature.com/public/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/request-oauth-authorization-code.md) for the provider-specific parameters and requirements.

