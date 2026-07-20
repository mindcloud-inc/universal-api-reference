# <img src="https://images.mindcloud.co/apps/icons/iubenda_1773867295268.png" alt="iubenda logo" width="28" height="28"> iubenda: Universal API

Connect to the iubenda Consent Database HTTP API to manage consents, subjects, legal notices, and consent proof documents.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/iubenda/latest
- **Category:** Productivity / Legal & Contracts
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.iubenda.com/
- **Vendor API docs:** https://www.iubenda.com/en/help/6484-consent-solution-http-api-documentation/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Subjects](actions/list-subjects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iubenda/latest/actions/list-subjects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Consent

| Action | Method | Description |
| --- | --- | --- |
| [Create Consent](actions/create-consent.md) | POST | Creates a consent in iubenda. |
| [Get Consent](actions/get-consent.md) | GET | Retrieves a consent from iubenda. |
| [Get Latest Consent for Subject](actions/get-latest-consent-for-subject.md) | GET | Retrieves the latest consent for a subject from iubenda. |
| [List Consents](actions/list-consents.md) | GET | Retrieves consents from iubenda. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Create Document](actions/create-document.md) | POST | Creates a document in iubenda. |
| [Get Document](actions/get-document.md) | GET | Retrieves a document from iubenda. |
| [List Documents](actions/list-documents.md) | GET | Retrieves documents from iubenda. |

### Legal Notice

| Action | Method | Description |
| --- | --- | --- |
| [Create Legal Notice](actions/create-legal-notice.md) | POST | Creates a legal notice in iubenda. |
| [Get Legal Notice Version](actions/get-legal-notice-version.md) | GET | Retrieves a legal notice version from iubenda. |
| [List Legal Notice Versions](actions/list-legal-notice-versions.md) | GET | Retrieves legal notice versions from iubenda. |
| [List Legal Notices](actions/list-legal-notices.md) | GET | Retrieves legal notices from iubenda. |

### Subject

| Action | Method | Description |
| --- | --- | --- |
| [Create Subject](actions/create-subject.md) | POST | Creates a subject in iubenda. |
| [Get Subject](actions/get-subject.md) | GET | Retrieves a subject from iubenda. |
| [List Subjects](actions/list-subjects.md) | GET | Retrieves subjects from iubenda. |
| [Update Subject](actions/update-subject.md) | PUT | Updates a subject in iubenda. |

