# <img src="https://images.mindcloud.co/apps/icons/6315c8fb267b7df328cef873-theswarm-symbol-favicon_1774977991372.png" alt="Swarm logo" width="28" height="28"> Swarm: Universal API

The Swarm is a relationship intelligence platform for searching professional profiles and companies, fetching detailed records, and finding warm introductions through your team's network.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/swarm/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.theswarm.com
- **Vendor API docs:** https://docs.theswarm.com/docs/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Refresh Profile](actions/refresh-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/swarm/latest/actions/refresh-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Get Post Comments](actions/get-post-comments.md) | GET | Retrieves comments for a post from Swarm. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Companies](actions/fetch-companies.md) | GET | Retrieves companies from Swarm by company ID. |
| [Search Companies](actions/search-companies.md) | GET | Finds companies in Swarm using an OpenSearch query. |

### Profile

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Profiles](actions/fetch-profiles.md) | GET | Retrieves profiles from Swarm by profile ID. |
| [Refresh Profile](actions/refresh-profile.md) | GET | Refreshes a profile in Swarm by LinkedIn username. |
| [Search Profiles](actions/search-profiles.md) | GET | Finds profiles in Swarm using an OpenSearch query. |

### Reaction

| Action | Method | Description |
| --- | --- | --- |
| [Get Post Reactions](actions/get-post-reactions.md) | GET | Retrieves reactions for a post from Swarm. |

### Reshare

| Action | Method | Description |
| --- | --- | --- |
| [Get Post Reshares](actions/get-post-reshares.md) | GET | Retrieves reshares for a post from Swarm. |

### Social Post

| Action | Method | Description |
| --- | --- | --- |
| [Get Profile Posts](actions/get-profile-posts.md) | GET | Retrieves profile posts from Swarm by LinkedIn ID. |

### Warm Path

| Action | Method | Description |
| --- | --- | --- |
| [Find Warm Paths by Company Name](actions/find-warm-paths-by-company-name.md) | GET | Finds warm paths in Swarm by company name. |
| [Find Warm Paths by Company Website](actions/find-warm-paths-by-company-website.md) | GET | Finds warm paths in Swarm by company website. |
| [Find Warm Paths by LinkedIn URL](actions/find-warm-paths-by-linkedin-url.md) | GET | Finds warm paths in Swarm by LinkedIn URL. |

