# <img src="https://images.mindcloud.co/apps/icons/quiltt_1775223973553.png" alt="Quiltt logo" width="28" height="28"> Quiltt: Universal API

Quiltt is a unified open banking API for profile management, connector orchestration, and financial data access across multiple providers.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/quiltt/latest
- **Category:** Commerce / Payments & Billing
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.quiltt.io
- **Vendor API docs:** https://www.quiltt.dev/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Profiles](actions/list-profiles.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quiltt/latest/actions/list-profiles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Create Straddle Processor Token](actions/create-straddle-processor-token.md) | POST |  |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Check Session Token](actions/check-session-token.md) | GET |  |
| [Issue Session Token](actions/issue-session-token.md) | POST |  |
| [Issue Session Token For New Profile](actions/issue-session-token-for-new-profile.md) | POST |  |
| [Revoke Session Token](actions/revoke-session-token.md) | DELETE |  |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook Subscription](actions/create-webhook-subscription.md) | POST |  |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Create Profile](actions/create-profile.md) | POST |  |
| [Delete Profile](actions/delete-profile.md) | DELETE |  |
| [Get Profile](actions/get-profile.md) | GET |  |
| [List Profiles](actions/list-profiles.md) | GET |  |
| [Update Profile](actions/update-profile.md) | PUT |  |

