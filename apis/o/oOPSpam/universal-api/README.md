# <img src="https://images.mindcloud.co/apps/icons/images-1_1773939521280.png" alt="OOPSpam logo" width="28" height="28"> OOPSpam: Universal API

OOPSpam is an anti-spam API for classifying form submissions, reporting false positives/negatives, and checking domain reputation.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/oOPSpam/latest
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.oopspam.com/
- **Vendor API docs:** https://www.oopspam.com/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check Domain Reputation](actions/check-domain-reputation.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oOPSpam/latest/actions/check-domain-reputation?connectionId=$CONNECTION_ID&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Domain Reputation

| Action | Method | Description |
| --- | --- | --- |
| [Check Domain Reputation](actions/check-domain-reputation.md) | GET | Checks a domain's reputation in OOPSpam. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Check Content for Spam](actions/check-content-for-spam.md) | POST | Checks submitted content for spam in OOPSpam. |
| [Report Misdetection](actions/report-misdetection.md) | POST | Reports a false positive or false negative to OOPSpam. |

