# <img src="https://images.mindcloud.co/apps/icons/reverse-contact_1774648993191.png" alt="Reverse Contact logo" width="28" height="28"> Reverse Contact: Universal API

Find people, companies, emails, and social profile data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/reverseContact/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.reversecontact.com
- **Vendor API docs:** https://app.reversecontact.com/docs/endpoints

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Usage](actions/get-usage.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reverseContact/latest/actions/get-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Person Comments](actions/fetch-person-comments.md) | GET |  |
| [Fetch Post Comments](actions/fetch-post-comments.md) | GET |  |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Check Company Profile Status](actions/check-company-profile-status.md) | GET |  |
| [Fetch Company Posts](actions/fetch-company-posts.md) | GET |  |
| [Fetch Company Profile](actions/fetch-company-profile.md) | GET |  |
| [Fetch Company Profile Live](actions/fetch-company-profile-live.md) | GET |  |
| [Resolve Company From Domain](actions/resolve-company-from-domain.md) | GET |  |
| [Search Companies](actions/search-companies.md) | GET |  |

### Email

| Action | Method | Description |
| --- | --- | --- |
| [Find Professional Email](actions/find-professional-email.md) | GET |  |
| [Verify Email](actions/verify-email.md) | GET |  |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Check Person Profile Status](actions/check-person-profile-status.md) | GET |  |
| [Fetch Person Profile](actions/fetch-person-profile.md) | GET |  |
| [Fetch Person Profile Live](actions/fetch-person-profile-live.md) | GET |  |
| [Resolve Person From Email](actions/resolve-person-from-email.md) | GET |  |
| [Resolve Person From Name](actions/resolve-person-from-name.md) | GET |  |
| [Search Persons](actions/search-persons.md) | GET |  |

### Post

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Person Posts](actions/fetch-person-posts.md) | GET |  |
| [Fetch Post Details](actions/fetch-post-details.md) | GET |  |

### Reaction

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Person Reactions](actions/fetch-person-reactions.md) | GET |  |

### Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Usage](actions/get-usage.md) | GET |  |

