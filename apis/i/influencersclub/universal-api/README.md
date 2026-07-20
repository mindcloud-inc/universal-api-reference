# <img src="https://images.mindcloud.co/apps/icons/screenshot-2026-04-01-at-16_1775073118297.png" alt="Influencers.club logo" width="28" height="28"> Influencers.club: Universal API

Discover creators and enrich social profiles with creator data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/influencersclub/latest
- **Category:** Marketing
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://influencers.club
- **Vendor API docs:** https://docs.influencers.club

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Retrieve Account Credits And Usage](actions/retrieve-account-credits-and-usage.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/retrieve-account-credits-and-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Accountcredits

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Account Credits And Usage](actions/retrieve-account-credits-and-usage.md) | GET | Retrieves account credits and usage details from Influencers.club. |

### Audiencebrandcategories

| Action | Method | Description |
| --- | --- | --- |
| [List Audience Brand Categories](actions/list-audience-brand-categories.md) | GET | Retrieves audience brand categories from Influencers.club. |

### Audiencebrandnames

| Action | Method | Description |
| --- | --- | --- |
| [List Audience Brand Names](actions/list-audience-brand-names.md) | GET | Retrieves audience brand names from Influencers.club. |

### Audienceinterests

| Action | Method | Description |
| --- | --- | --- |
| [List Audience Interests](actions/list-audience-interests.md) | GET | Retrieves audience interests from Influencers.club. |

### Audiencelocations

| Action | Method | Description |
| --- | --- | --- |
| [List Audience Locations](actions/list-audience-locations.md) | GET | Retrieves audience locations from Influencers.club. |

### Audienceoverlap

| Action | Method | Description |
| --- | --- | --- |
| [Compare Creator Audience Overlap](actions/compare-creator-audience-overlap.md) | GET | Retrieves audience overlap metrics for multiple creators in Influencers.club. |

### Connectedsocials

| Action | Method | Description |
| --- | --- | --- |
| [Find Creator Connected Socials](actions/find-creator-connected-socials.md) | GET | Finds verified connected social accounts for a creator in Influencers.club. |

### Creatorpostdetails

| Action | Method | Description |
| --- | --- | --- |
| [Get Creator Content Details](actions/get-creator-content-details.md) | GET | Retrieves detailed metrics for specific creator content in Influencers.club. |

### Creatorposts

| Action | Method | Description |
| --- | --- | --- |
| [List Creator Content Posts](actions/list-creator-content-posts.md) | GET | Retrieves recent creator posts from Influencers.club by platform and handle. |

### Creatorsearch

| Action | Method | Description |
| --- | --- | --- |
| [Search Creators (Discovery)](actions/search-creators-discovery.md) | GET | Finds creators in Influencers.club by platform-specific discovery filters. |

### Discoverybrands

| Action | Method | Description |
| --- | --- | --- |
| [List Discovery Brands](actions/list-discovery-brands.md) | GET | Retrieves discovery brand filters from Influencers.club. |

### Discoverygames

| Action | Method | Description |
| --- | --- | --- |
| [List Discovery Games](actions/list-discovery-games.md) | GET | Retrieves Twitch game filters from Influencers.club. |

### Discoverylanguages

| Action | Method | Description |
| --- | --- | --- |
| [List Discovery Languages](actions/list-discovery-languages.md) | GET | Retrieves supported discovery languages from Influencers.club. |

### Discoverylocations

| Action | Method | Description |
| --- | --- | --- |
| [List Discovery Locations By Platform](actions/list-discovery-locations-by-platform.md) | GET | Retrieves discovery locations for a platform from Influencers.club. |

### Discoveryyoutubetopics

| Action | Method | Description |
| --- | --- | --- |
| [List Discovery YouTube Topics](actions/list-discovery-youtube-topics.md) | GET | Retrieves YouTube discovery topics from Influencers.club. |

### Enrichedcreatoremail

| Action | Method | Description |
| --- | --- | --- |
| [Enrich Creator By Email](actions/enrich-creator-by-email.md) | GET | Retrieves creator enrichment data from Influencers.club by email address. |

### Enrichedcreatorfull

| Action | Method | Description |
| --- | --- | --- |
| [Enrich Creator By Handle (Full)](actions/enrich-creator-by-handle-full.md) | GET | Retrieves full creator enrichment data from Influencers.club by handle. |

### Enrichedcreatorraw

| Action | Method | Description |
| --- | --- | --- |
| [Enrich Creator By Handle (Raw)](actions/enrich-creator-by-handle-raw.md) | GET | Retrieves raw creator profile data from Influencers.club by handle. |

### Enrichmentbatch

| Action | Method | Description |
| --- | --- | --- |
| [Create Enrichment Batch](actions/create-enrichment-batch.md) | POST | Creates a batch enrichment job in Influencers.club from a CSV. |

### Enrichmentbatchresult

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Enrichment Batch Results](actions/retrieve-enrichment-batch-results.md) | GET | Retrieves batch enrichment results from Influencers.club. |

### Enrichmentbatchresume

| Action | Method | Description |
| --- | --- | --- |
| [Resume Enrichment Batch](actions/resume-enrichment-batch.md) | PUT | Resumes a paused batch enrichment job in Influencers.club. |

### Enrichmentbatchstatus

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Enrichment Batch Status](actions/retrieve-enrichment-batch-status.md) | GET | Retrieves batch enrichment job status from Influencers.club. |

### Similarcreators

| Action | Method | Description |
| --- | --- | --- |
| [Find Similar Creators](actions/find-similar-creators.md) | GET | Finds creators similar to a reference creator in Influencers.club. |

