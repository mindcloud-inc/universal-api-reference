# <img src="https://images.mindcloud.co/apps/icons/storyscale_1775508756914.png" alt="Storyscale logo" width="28" height="28"> Storyscale: Universal API

Interactive product demo software for SaaS teams to create product tours, manage demo content, and engage prospects.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/storyscale/latest
- **Category:** Marketing
- **Actions:** 41
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.storyscale.com
- **Vendor API docs:** https://prodapi.storyscale.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Experiences, Sequences, and Assets](actions/search-experiences-sequences-and-assets.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/storyscale/latest/actions/search-experiences-sequences-and-assets?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (41)

### Access Token

| Action | Method | Description |
| --- | --- | --- |
| [Get Access Token](actions/get-access-token.md) | GET |  |

### Asset Type

| Action | Method | Description |
| --- | --- | --- |
| [List Asset Types](actions/list-asset-types.md) | GET |  |

### Experience

| Action | Method | Description |
| --- | --- | --- |
| [Add Sequence To Experience](actions/add-sequence-to-experience.md) | PUT |  |
| [Create Experience](actions/create-experience.md) | POST |  |
| [Delete Experience](actions/delete-experience.md) | DELETE |  |
| [Get Experience](actions/get-experience.md) | GET |  |
| [List All Experiences](actions/list-all-experiences.md) | GET |  |
| [List Experiences](actions/list-experiences.md) | GET |  |
| [List Experiences with Filters](actions/list-experiences-with-filters.md) | GET |  |
| [List Sequence Experiences](actions/list-sequence-experiences.md) | GET |  |
| [Update Experience](actions/update-experience.md) | PUT |  |

### Experience Type

| Action | Method | Description |
| --- | --- | --- |
| [List Experience Types](actions/list-experience-types.md) | GET |  |

### Library Asset

| Action | Method | Description |
| --- | --- | --- |
| [Create Library Asset](actions/create-library-asset.md) | POST |  |
| [Delete Library Asset](actions/delete-library-asset.md) | DELETE |  |
| [Get Library Asset](actions/get-library-asset.md) | GET |  |
| [List Library Assets](actions/list-library-assets.md) | GET |  |
| [Search Library Assets](actions/search-library-assets.md) | GET |  |
| [Update Library Asset](actions/update-library-asset.md) | PUT |  |
| [Update Library Asset Tags](actions/update-library-asset-tags.md) | PUT |  |

### Platform Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Platform Tags](actions/list-platform-tags.md) | GET |  |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Experiences, Sequences, and Assets](actions/search-experiences-sequences-and-assets.md) | GET |  |

### Sequence

| Action | Method | Description |
| --- | --- | --- |
| [Add Assets To Sequences](actions/add-assets-to-sequences.md) | PUT |  |
| [Create Sequence](actions/create-sequence.md) | POST |  |
| [Delete Sequence](actions/delete-sequence.md) | DELETE |  |
| [Get Sequence](actions/get-sequence.md) | GET |  |
| [List All Sequences](actions/list-all-sequences.md) | GET |  |
| [List Sequences](actions/list-sequences.md) | GET |  |
| [Update Sequence](actions/update-sequence.md) | PUT |  |

### Style Guide

| Action | Method | Description |
| --- | --- | --- |
| [Create Style Guide](actions/create-style-guide.md) | POST |  |
| [Delete Style Guide](actions/delete-style-guide.md) | DELETE |  |
| [Get Style Guide](actions/get-style-guide.md) | GET |  |
| [List Style Guides](actions/list-style-guides.md) | GET |  |
| [Update Style Guide](actions/update-style-guide.md) | PUT |  |

### Target Audience Segment

| Action | Method | Description |
| --- | --- | --- |
| [List Target Audience Segments](actions/list-target-audience-segments.md) | GET |  |

### Tour

| Action | Method | Description |
| --- | --- | --- |
| [Clone Tour](actions/clone-tour.md) | POST |  |
| [Create Tour](actions/create-tour.md) | POST |  |
| [Delete Tour](actions/delete-tour.md) | DELETE |  |
| [Get Tour](actions/get-tour.md) | GET |  |
| [List Tours](actions/list-tours.md) | GET |  |
| [Publish Tour](actions/publish-tour.md) | PUT |  |
| [Update Tour](actions/update-tour.md) | PUT |  |

