# <img src="https://images.mindcloud.co/apps/icons/invite-referrals_1775059458592.png" alt="InviteReferrals logo" width="28" height="28"> InviteReferrals: Universal API

InviteReferrals referral marketing API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/inviteReferrals/latest
- **Category:** Marketing
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.invitereferrals.com
- **Vendor API docs:** https://docs.invitereferrals.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Add Conversion](actions/add-conversion.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/inviteReferrals/latest/actions/add-conversion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderId": "string",
  "campaignId": 1,
  "refereeName": "Ava Chen",
  "refereeEmail": "ava@example.com"
}'
```

## Actions (2)

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Add Conversion](actions/add-conversion.md) | POST |  |
| [Approve Or Reject Conversion](actions/approve-or-reject-conversion.md) | PUT |  |

