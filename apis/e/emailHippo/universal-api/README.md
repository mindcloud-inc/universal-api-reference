# <img src="https://images.mindcloud.co/apps/icons/email-hippo-icon-square_1775851331017.png" alt="Email Hippo logo" width="28" height="28"> Email Hippo: Universal API

Email Hippo MORE email verification and quota APIs for validating email addresses and checking remaining license usage.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/emailHippo/latest
- **Category:** IT Operations / Security & Compliance
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.emailhippo.com/
- **Vendor API docs:** https://docs.emailhippo.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Quota Usage](actions/get-quota-usage.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emailHippo/latest/actions/get-quota-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Email Verification

| Action | Method | Description |
| --- | --- | --- |
| [Verify Email (MORE V2)](actions/verify-email-morev2.md) | GET | Verifies an email address with Email Hippo MORE V2. |
| [Verify Email (MORE V3 BSON)](actions/verify-email-morev3-bson.md) | GET | Verifies an email address with Email Hippo MORE V3 BSON. |
| [Verify Email (MORE V3 JSON)](actions/verify-email-morev3-json.md) | GET | Verifies an email address with Email Hippo MORE V3 JSON. |
| [Verify Email (MORE V3 Protobuf)](actions/verify-email-morev3-protobuf.md) | GET | Verifies an email address with Email Hippo MORE V3 Protobuf. |
| [Verify Email (MORE V3 XML)](actions/verify-email-morev3-xml.md) | GET | Verifies an email address with Email Hippo MORE V3 XML. |

### Quota Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Quota Usage](actions/get-quota-usage.md) | GET | Retrieves quota usage details from Email Hippo. |

