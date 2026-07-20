# Appwrite: Create OAuth2 token

Creates a new OAuth2 token in your Appwrite project.

```
GET https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/account-create-oauth2-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/account-create-oauth2-token?connectionId=$CONNECTION_ID&provider=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "provider": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/account-create-oauth2-token?${params}`, {
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
| `provider` | string | yes | OAuth2 Provider. Currently, supported providers are: amazon, apple, auth0, authentik, autodesk, bitbucket, bitly, box, dailymotion, discord, disqus, dropbox, etsy, facebook, figma, github, gitlab, google, linkedin, microsoft, notion, oidc, okta, paypal, paypalSandbox, podio, salesforce, slack, spotify, stripe, tradeshift, tradeshiftBox, twitch, wordpress, yahoo, yammer, yandex, zoho, zoom. |
| `success` | string | no | URL to redirect back to your app after a successful login attempt. Only URLs from hostnames in your project's platform list are allowed. This requirement helps to prevent an [open redirect](https://cheatsheetseries.owasp.org/cheatsheets/Unvalidated_Redirects_and_Forwards_Cheat_Sheet.html) attack against your project API. |
| `failure` | string | no | URL to redirect back to your app after a failed login attempt. Only URLs from hostnames in your project's platform list are allowed. This requirement helps to prevent an [open redirect](https://cheatsheetseries.owasp.org/cheatsheets/Unvalidated_Redirects_and_Forwards_Cheat_Sheet.html) attack against your project API. |
| `scopes[]` | array<string> | no | A list of custom OAuth2 scopes. Check each provider internal docs for a list of supported scopes. Maximum of 100 scopes are allowed, each 4096 characters long. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object | Provider response payload. |

## Native endpoint

Through the native Appwrite API, this operation is `GET /account/tokens/oauth2/{provider}` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/account-create-oauth2-token.md) for the provider-specific parameters and requirements.

