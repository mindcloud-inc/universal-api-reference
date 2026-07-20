# <img src="https://images.mindcloud.co/apps/icons/los-angeles-times_1776426969843.png" alt="Los Angeles Times logo" width="28" height="28"> Los Angeles Times: Universal API

Browse Los Angeles Times RSS feeds and retrieve the latest published stories by section.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/losAngelesTimes/latest
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.latimes.com
- **Vendor API docs:** https://www.latimes.com/feeds

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Business Stories](actions/list-business-stories.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/losAngelesTimes/latest/actions/list-business-stories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Story

| Action | Method | Description |
| --- | --- | --- |
| [List Autos Stories](actions/list-autos-stories.md) | GET | Retrieves Los Angeles Times autos stories. |
| [List Awards Stories](actions/list-awards-stories.md) | GET | Retrieves Los Angeles Times awards stories. |
| [List Books Stories](actions/list-books-stories.md) | GET | Retrieves Los Angeles Times books stories. |
| [List Business Stories](actions/list-business-stories.md) | GET | Retrieves Los Angeles Times business stories. |
| [List California Stories](actions/list-california-stories.md) | GET | Retrieves Los Angeles Times California stories. |
| [List Climate and Environment Stories](actions/list-climate-and-environment-stories.md) | GET | Retrieves Los Angeles Times climate and environment stories. |
| [List Clippers Stories](actions/list-clippers-stories.md) | GET | Retrieves Los Angeles Times Clippers stories. |
| [List Company Town Stories](actions/list-company-town-stories.md) | GET | Retrieves Los Angeles Times Company Town stories. |
| [List Dodgers Stories](actions/list-dodgers-stories.md) | GET | Retrieves Los Angeles Times Dodgers stories. |
| [List Entertainment and Arts Stories](actions/list-entertainment-and-arts-stories.md) | GET | Retrieves Los Angeles Times entertainment and arts stories. |
| [List Food Stories](actions/list-food-stories.md) | GET | Retrieves Los Angeles Times food stories. |
| [List High School Sports Stories](actions/list-high-school-sports-stories.md) | GET | Retrieves Los Angeles Times high school sports stories. |
| [List Lakers Stories](actions/list-lakers-stories.md) | GET | Retrieves Los Angeles Times Lakers stories. |
| [List Lifestyle Stories](actions/list-lifestyle-stories.md) | GET | Retrieves Los Angeles Times lifestyle stories. |
| [List Movies Stories](actions/list-movies-stories.md) | GET | Retrieves Los Angeles Times movies stories. |
| [List Music Stories](actions/list-music-stories.md) | GET | Retrieves Los Angeles Times music stories. |
| [List Obituaries](actions/list-obituaries.md) | GET | Retrieves Los Angeles Times obituary stories. |
| [List Opinion Stories](actions/list-opinion-stories.md) | GET | Retrieves Los Angeles Times opinion stories. |
| [List Orange County Stories](actions/list-orange-county-stories.md) | GET | Retrieves Los Angeles Times Orange County stories. |
| [List Politics Stories](actions/list-politics-stories.md) | GET | Retrieves Los Angeles Times politics stories. |
| [List Rams Stories](actions/list-rams-stories.md) | GET | Retrieves Los Angeles Times Rams stories. |
| [List Real Estate Stories](actions/list-real-estate-stories.md) | GET | Retrieves Los Angeles Times real estate stories. |
| [List Science Stories](actions/list-science-stories.md) | GET | Retrieves Los Angeles Times science stories. |
| [List Sports Stories](actions/list-sports-stories.md) | GET | Retrieves Los Angeles Times sports stories. |
| [List Technology Stories](actions/list-technology-stories.md) | GET | Retrieves Los Angeles Times technology stories. |
| [List Travel Stories](actions/list-travel-stories.md) | GET | Retrieves Los Angeles Times travel stories. |
| [List TV Stories](actions/list-tv-stories.md) | GET | Retrieves Los Angeles Times TV stories. |
| [List UCLA Stories](actions/list-ucla-stories.md) | GET | Retrieves Los Angeles Times UCLA stories. |
| [List USC Stories](actions/list-usc-stories.md) | GET | Retrieves Los Angeles Times USC stories. |
| [List World and Nation Stories](actions/list-world-and-nation-stories.md) | GET | Retrieves Los Angeles Times world and nation stories. |

