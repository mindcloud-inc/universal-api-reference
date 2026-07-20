# <img src="https://images.mindcloud.co/apps/icons/download-1_1775505216253.png" alt="Virtual Summits Software logo" width="28" height="28"> Virtual Summits Software: Universal API

Access summit, presentation, sponsor, landing page, session, and attendee data from Virtual Summits Software.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/virtualSummitsSoftware/latest
- **Category:** Marketing / Events & Webinars
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://virtualsummits.com/
- **Vendor API docs:** https://support.virtualsummits.com/hc/en-us/sections/360013135012-Integrations

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Summit Attendees](actions/list-summit-attendees.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/virtualSummitsSoftware/latest/actions/list-summit-attendees?connectionId=$CONNECTION_ID&summitId=4463" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Attendees

| Action | Method | Description |
| --- | --- | --- |
| [List Summit Attendees](actions/list-summit-attendees.md) | GET |  |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [List Summit Categories](actions/list-summit-categories.md) | GET |  |

### Landing Pages

| Action | Method | Description |
| --- | --- | --- |
| [List Summit Landing Pages](actions/list-summit-landing-pages.md) | GET |  |

### Presentations

| Action | Method | Description |
| --- | --- | --- |
| [List Summit Presentations](actions/list-summit-presentations.md) | GET |  |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [List Summit Sessions](actions/list-summit-sessions.md) | GET |  |

### Speaker Applications

| Action | Method | Description |
| --- | --- | --- |
| [List Speaker Application Questions](actions/list-speaker-application-questions.md) | GET |  |

### Sponsors

| Action | Method | Description |
| --- | --- | --- |
| [List Sponsorship Tiers](actions/list-sponsorship-tiers.md) | GET |  |
| [List Summit Sponsors](actions/list-summit-sponsors.md) | GET |  |

### Summits

| Action | Method | Description |
| --- | --- | --- |
| [Get Summit](actions/get-summit.md) | GET |  |
| [List Summits](actions/list-summits.md) | GET |  |

### Tiers

| Action | Method | Description |
| --- | --- | --- |
| [List Tier Items](actions/list-tier-items.md) | GET |  |
| [List Tier Levels](actions/list-tier-levels.md) | GET |  |

