# <img src="https://images.mindcloud.co/apps/icons/pass-kit-mailchimp-partners_1773780937821.png" alt="PassKit Membership logo" width="28" height="28"> PassKit Membership: Universal API

PassKit Membership lets teams issue and manage digital membership passes, members, tiers, balances, and member events through PassKit's membership APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/passKitMembership/latest
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://passkit.com
- **Vendor API docs:** https://docs.passkit.io/protocols/member/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Programs](actions/list-programs.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/passKitMembership/latest/actions/list-programs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Member

| Action | Method | Description |
| --- | --- | --- |
| [Create Member](actions/create-member.md) | POST | Creates a member in PassKit Membership. |
| [Delete Member](actions/delete-member.md) | DELETE | Deletes an existing member from PassKit Membership. |
| [Find Member By External ID](actions/find-member-by-external-id.md) | GET | Finds a member in PassKit Membership by external ID. |
| [Get Member By External ID](actions/get-member-by-external-id.md) | GET | Retrieves a member from PassKit Membership by external ID. |
| [List Members](actions/list-members.md) | GET | Retrieves members from a PassKit Membership program. |
| [Set Member Points By External ID](actions/set-member-points-by-external-id.md) | PUT | Updates a member's points in PassKit Membership by external ID. |
| [Set Member Secondary Points By External ID](actions/set-member-secondary-points-by-external-id.md) | PUT | Updates a member's secondary points in PassKit Membership by external ID. |
| [Set Member Tier Points By External ID](actions/set-member-tier-points-by-external-id.md) | PUT | Updates a member's tier points in PassKit Membership by external ID. |
| [Update Member](actions/update-member.md) | PUT | Updates an existing member in PassKit Membership. |
| [Update Member By External ID](actions/update-member-by-external-id.md) | PUT | Updates an existing member in PassKit Membership by external ID. |

### Member Count

| Action | Method | Description |
| --- | --- | --- |
| [Count Members](actions/count-members.md) | GET | Retrieves a filtered member count from a PassKit Membership program. |
| [Count Members By External ID](actions/count-members-by-external-id.md) | GET | Retrieves a member count by external ID in PassKit Membership. |

### Program

| Action | Method | Description |
| --- | --- | --- |
| [List Programs](actions/list-programs.md) | GET | Retrieves membership programs from PassKit Membership. |

### Tier

| Action | Method | Description |
| --- | --- | --- |
| [List Tiers](actions/list-tiers.md) | GET | Retrieves membership tiers from a PassKit Membership program. |

