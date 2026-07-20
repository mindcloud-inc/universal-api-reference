# <img src="https://images.mindcloud.co/apps/icons/issue-badge_1775079793026.png" alt="IssueBadge logo" width="28" height="28"> IssueBadge: Universal API

Create, issue, and verify digital badges and certificates

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/issueBadge/latest
- **Category:** Human Resources / Learning (LMS)
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://issuebadge.com/
- **Vendor API docs:** https://app.issuebadge.com/docs/api-documentation.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Badges](actions/list-badges.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/issueBadge/latest/actions/list-badges?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Badge

| Action | Method | Description |
| --- | --- | --- |
| [Create Badge](actions/create-badge.md) | POST |  |
| [List Badges](actions/list-badges.md) | GET |  |

### Badge Issuance

| Action | Method | Description |
| --- | --- | --- |
| [Issue Badge to Recipient](actions/issue-badge-to-recipient.md) | POST |  |

