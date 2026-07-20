# Vortex: Native API Reference

A consolidated summary of Vortex's API configuration and 16 documented operations, with links to official documentation.

- **Official docs:** https://docs.vortexsoftware.com
- **OpenAPI specification:** https://api.vortexsoftware.com/api-json
- **API base URL:** `https://api.vortexsoftware.com`

## Authentication

### API Key Header

Use your Vortex API key. MindCloud sends it as the X-API-Key header for every request.

### Credentials

- **API Key:** `apiKey` · required · Your Vortex API key.

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://docs.vortexsoftware.com)

## Endpoints (16 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Accept Invitation](actions/accept-invitation.md) | `POST /api/v1/invitations/accept` | [docs](https://docs.vortexsoftware.com/api-reference/invitations/accept-an-invitation) |
| [Configure Autojoin Domains](actions/configure-autojoin-domains.md) | `POST /api/v1/invitations/autojoin` | [docs](https://docs.vortexsoftware.com/api-reference/invitations--autojoin/configure-autojoin-domains-for-a-target-scope) |
| [Create Invitation](actions/create-invitation.md) | `POST /api/v1/invitations` | [docs](https://docs.vortexsoftware.com/api-reference/invitations/create-an-invitation) |
| [Delete Autojoin Domain](actions/delete-autojoin-domain.md) | `DELETE /api/v1/invitations/autojoin/{id}` | [docs](https://docs.vortexsoftware.com/api-reference/invitations--autojoin/delete-autojoin-domain) |
| [Delete Invitation](actions/delete-invitation.md) | `DELETE /api/v1/invitations/{invitationId}` | [docs](https://docs.vortexsoftware.com/api-reference/invitations/delete-an-invitation) |
| [Delete Invitations By Group](actions/delete-invitations-by-group.md) | `DELETE /api/v1/invitations/by-group/{groupType}/{groupId}` | [docs](https://docs.vortexsoftware.com) |
| [Delete Invitations By Scope](actions/delete-invitations-by-scope.md) | `DELETE /api/v1/invitations/by-scope/{scopeType}/{scope}` | [docs](https://docs.vortexsoftware.com/api-reference/invitations/delete-all-invitations-by-scope) |
| [Get Autojoin Domain By Id](actions/get-autojoin-domain-by-id.md) | `GET /api/v1/invitations/autojoin/{id}` | [docs](https://docs.vortexsoftware.com/api-reference/invitations--autojoin/get-autojoin-domain-by-id) |
| [Get Autojoin Domains By Scope](actions/get-autojoin-domains-by-scope.md) | `GET /api/v1/invitations/by-scope/{scopeType}/{scope}/autojoin` | [docs](https://docs.vortexsoftware.com/api-reference/invitations--autojoin/get-autojoin-domains-for-a-specific-scope) |
| [Get Autojoin Invitations By Domain](actions/get-autojoin-invitations-by-domain.md) | `GET /api/v1/invitations/autojoin/by-domain/{domain}` | [docs](https://docs.vortexsoftware.com/api-reference/invitations--autojoin/get-autojoin-invitations-by-domain) |
| [Get Invitation](actions/get-invitation.md) | `GET /api/v1/invitations/{invitationId}` | [docs](https://docs.vortexsoftware.com/api-reference/invitations/get-an-invitation-by-id) |
| [List Open Invitations By Group](actions/list-open-invitations-by-group.md) | `GET /api/v1/invitations/by-group/{groupType}/{groupId}` | [docs](https://docs.vortexsoftware.com) |
| [List Open Invitations By Scope](actions/list-open-invitations-by-scope.md) | `GET /api/v1/invitations/by-scope/{scopeType}/{scope}` | [docs](https://docs.vortexsoftware.com/api-reference/invitations/get-open-invitations-by-scope) |
| [List Open Invitations For Invitee](actions/list-open-invitations-for-invitee.md) | `GET /api/v1/invitations` | [docs](https://docs.vortexsoftware.com/api-reference/invitations/get-open-invitations-for-an-invitee) |
| [Reinvite Invitation](actions/reinvite-invitation.md) | `POST /api/v1/invitations/{invitationId}/reinvite` | [docs](https://docs.vortexsoftware.com/api-reference/invitations/re-send-an-invitation) |
| [Sync Internal Invitation Decision](actions/sync-internal-invitation-decision.md) | `POST /api/v1/invitations/sync-internal-invitation` | [docs](https://docs.vortexsoftware.com/api-reference/invitations/sync-an-internal-invitation-decision-from-an-external-system) |
