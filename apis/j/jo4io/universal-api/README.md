# <img src="https://images.mindcloud.co/apps/icons/jo4io_1775246772053.png" alt="jo4.io logo" width="28" height="28"> jo4.io: Universal API

jo4.io is a URL shortener and link management API for creating short links, tracking conversions, managing custom domains, webhooks, API keys, teams, and transfer requests.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/jo4io/latest
- **Category:** Marketing
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://jo4.io
- **Vendor API docs:** https://jo4-api.jo4.io/swagger-ui/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List API Keys](actions/list-api-keys.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/list-api-keys?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### A/b Test

| Action | Method | Description |
| --- | --- | --- |
| [Create A/B Test](actions/create-ab-test.md) | POST |  |
| [Declare A/B Test Winner](actions/declare-winner.md) | PUT |  |
| [Get A/B Test Stats](actions/get-ab-test-stats.md) | GET |  |
| [Pause A/B Test](actions/pause-ab-test.md) | PUT |  |
| [Promote A/B Test Winner](actions/promote-winner.md) | PUT |  |
| [Resume A/B Test](actions/resume-ab-test.md) | PUT |  |

### A/b Test Variant

| Action | Method | Description |
| --- | --- | --- |
| [Add A/B Test Variant](actions/add-variant.md) | POST |  |
| [List A/B Test Variants](actions/get-variants.md) | GET |  |

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Create API Key](actions/create-api-key.md) | POST |  |
| [List API Keys](actions/list-api-keys.md) | GET |  |

### Conversion

| Action | Method | Description |
| --- | --- | --- |
| [List Conversions](actions/get-conversions.md) | GET |  |
| [Record Conversion](actions/record-conversion-1.md) | POST |  |

### Domain

| Action | Method | Description |
| --- | --- | --- |
| [Add Domain](actions/add-domain.md) | POST |  |
| [List Domains](actions/get-domains.md) | GET |  |
| [Verify Domain](actions/verify-domain.md) | PUT |  |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Create Team](actions/create-team.md) | POST |  |
| [List My Teams](actions/get-my-teams.md) | GET |  |

### Team Invitation

| Action | Method | Description |
| --- | --- | --- |
| [List Team Invitations](actions/get-invitations.md) | GET |  |
| [Invite Member](actions/invite-member.md) | POST |  |

### Transfer Request

| Action | Method | Description |
| --- | --- | --- |
| [Approve Transfer Request](actions/approve-request.md) | PUT |  |
| [Create Transfer Request](actions/create-request.md) | POST |  |
| [Reject Transfer Request](actions/reject-request.md) | PUT |  |

### Url

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Import URLs](actions/bulk-import.md) | POST |  |
| [Create URL](actions/create-url.md) | POST |  |
| [Delete URL](actions/delete-url.md) | DELETE |  |
| [List My URLs](actions/get-my-urls.md) | GET |  |
| [Refresh URL Metadata](actions/refresh-metadata.md) | PUT |  |
| [Update URL](actions/update-url.md) | PUT |  |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST |  |
| [List My Webhooks](actions/get-my-webhooks.md) | GET |  |

