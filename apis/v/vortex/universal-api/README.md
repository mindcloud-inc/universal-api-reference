# <img src="https://images.mindcloud.co/apps/icons/apple-touch-icon-2_1775063193806.png" alt="Vortex logo" width="28" height="28"> Vortex: Universal API

Manage invitations and autojoin domain configuration in Vortex.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/vortex/latest
- **Actions:** 16
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.vortexsoftware.com
- **Vendor API docs:** https://docs.vortexsoftware.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Autojoin Domain By Id](actions/get-autojoin-domain-by-id.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vortex/latest/actions/get-autojoin-domain-by-id?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (16)

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Accept Invitation](actions/accept-invitation.md) | PUT |  |
| [Configure Autojoin Domains](actions/configure-autojoin-domains.md) | POST |  |
| [Create Invitation](actions/create-invitation.md) | POST |  |
| [Delete Autojoin Domain](actions/delete-autojoin-domain.md) | DELETE |  |
| [Delete Invitation](actions/delete-invitation.md) | DELETE |  |
| [Delete Invitations By Group](actions/delete-invitations-by-group.md) | DELETE |  |
| [Delete Invitations By Scope](actions/delete-invitations-by-scope.md) | DELETE |  |
| [Get Autojoin Domain By Id](actions/get-autojoin-domain-by-id.md) | GET |  |
| [Get Autojoin Domains By Scope](actions/get-autojoin-domains-by-scope.md) | GET |  |
| [Get Autojoin Invitations By Domain](actions/get-autojoin-invitations-by-domain.md) | GET |  |
| [Get Invitation](actions/get-invitation.md) | GET |  |
| [List Open Invitations By Group](actions/list-open-invitations-by-group.md) | GET |  |
| [List Open Invitations By Scope](actions/list-open-invitations-by-scope.md) | GET |  |
| [List Open Invitations For Invitee](actions/list-open-invitations-for-invitee.md) | GET |  |
| [Reinvite Invitation](actions/reinvite-invitation.md) | PUT |  |
| [Sync Internal Invitation Decision](actions/sync-internal-invitation-decision.md) | PUT |  |

