# Create OAuth2 token with Appwrite

Creates a new OAuth2 token in your Appwrite project.

## Endpoint

- **Method:** `GET`
- **Path:** `/account/tokens/oauth2/{provider}`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create OAuth2 token](https://appwrite.io/docs/references/cloud/server-rest/account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `provider` | path | `string` | yes | OAuth2 Provider. Currently, supported providers are: amazon, apple, auth0, authentik, autodesk, bitbucket, bitly, box, dailymotion, discord, disqus, dropbox, etsy, facebook, figma, github, gitlab, google, linkedin, microsoft, notion, oidc, okta, paypal, paypalSandbox, podio, salesforce, slack, spotify, stripe, tradeshift, tradeshiftBox, twitch, wordpress, yahoo, yammer, yandex, zoho, zoom. |
| `success` | query | `string` | no | URL to redirect back to your app after a successful login attempt.  Only URLs from hostnames in your project's platform list are allowed. This requirement helps to prevent an [open redirect](https://cheatsheetseries.owasp.org/cheatsheets/Unvalidated_Redirects_and_Forwards_Cheat_Sheet.html) attack against your project API. |
| `failure` | query | `string` | no | URL to redirect back to your app after a failed login attempt.  Only URLs from hostnames in your project's platform list are allowed. This requirement helps to prevent an [open redirect](https://cheatsheetseries.owasp.org/cheatsheets/Unvalidated_Redirects_and_Forwards_Cheat_Sheet.html) attack against your project API. |
| `scopes[]` | query | `array<string>` | no | A list of custom OAuth2 scopes. Check each provider internal docs for a list of supported scopes. Maximum of 100 scopes are allowed, each 4096 characters long. Send multiple values as a array. |
