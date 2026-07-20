# <img src="https://images.mindcloud.co/apps/icons/postmaster_1775736264551.png" alt="Postmaster+ logo" width="28" height="28"> Postmaster+: Universal API

Postmaster+ provides team-scoped email deliverability monitoring, email intelligence, blocklist scanning, and screenshot capture APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/postmaster/latest
- **Category:** Marketing
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://postmasterplus.app
- **Vendor API docs:** https://postmasterplus.app/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Retrieve Domains](actions/retrieve-domains.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/retrieve-domains?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Delete Single Email](actions/delete-single-email.md) | DELETE | Deletes single email intelligence from Postmaster+. |
| [Retrieve Single Email](actions/retrieve-single-email.md) | GET | Retrieves single email intelligence from Postmaster+. |
| [Scan Single Email](actions/scan-single-email.md) | POST | Scans a single email in Postmaster+. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Get Screenshot](actions/get-screenshot.md) | GET | Retrieves a screenshot from the Postmaster+ API. |
| [List Screenshots](actions/list-screenshots.md) | GET | Retrieves screenshots from the Postmaster+ API. |
| [Take Screenshot](actions/take-screenshot.md) | POST | Takes a screenshot with the Postmaster+ API. |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Blocklist Scan Status](actions/retrieve-blocklist-scan-status.md) | GET | Retrieves blocklist scan status from Postmaster+. |
| [Start Blocklist Scan](actions/start-blocklist-scan.md) | POST | Starts a blocklist scan in Postmaster+. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Domain](actions/retrieve-domain.md) | GET | Retrieves domain details from the Postmaster+ API. |
| [Retrieve Domain Feed](actions/retrieve-domain-feed.md) | GET | Retrieves feed items for a domain in Postmaster+. |
| [Retrieve Domains](actions/retrieve-domains.md) | GET | Retrieves available domains from the Postmaster+ API. |
| [Retrieve IPs](actions/retrieve-i-ps.md) | GET | Retrieves IP records from the Postmaster+ API. |
| [Retrieve IP](actions/retrieve-ip.md) | GET | Retrieves IP details from the Postmaster+ API. |
| [Retrieve IP Feed](actions/retrieve-ip-feed.md) | GET | Retrieves feed items for an IP in Postmaster+. |

