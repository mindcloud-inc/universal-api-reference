# iFormBuilder: Native API Reference

A consolidated summary of iFormBuilder's API configuration, with links to official documentation.

- **Official docs:** https://iformbuilder.docs.apiary.io/reference
- **API base URL:** `https://app.iformbuilder.com/exzact/api/v60`

## Authentication

### Custom JWT Bearer

Custom auth for iFormBuilder that mints an access token by signing a short-lived HS256 JWT bearer assertion at request time.

### Credentials

- **Client Key:** `clientId` · required · The iFormBuilder client key used as the JWT issuer and OAuth client ID.
- **Client Secret:** `clientSecret` · required · The iFormBuilder client secret used to sign the HS256 JWT bearer assertion.
- **ZIM User ID:** `zimUserId` · optional · Optional JWT subject claim. Leave blank unless your tenant requires a subject for token minting.

Send these headers with each API request:

```http
Authorization: Bearer <custom.access_token>
```

[Official authentication documentation](https://iformbuilder.docs.apiary.io/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.
