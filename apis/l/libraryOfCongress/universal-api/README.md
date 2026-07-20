# <img src="https://images.mindcloud.co/apps/icons/library-of-congress_1776429790794.png" alt="Library of Congress logo" width="28" height="28"> Library of Congress: Universal API

Search and retrieve public Library of Congress collections, items, resources, and collection metadata through the official loc.gov JSON/YAML API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/libraryOfCongress/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.loc.gov/
- **Vendor API docs:** https://www.loc.gov/apis/json-and-yaml/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Collection](actions/get-collection.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/libraryOfCongress/latest/actions/get-collection?connectionId=$CONNECTION_ID&collectionSlug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### 3d Object

| Action | Method | Description |
| --- | --- | --- |
| [Search 3D Objects](actions/search3d-objects.md) | GET | Finds 3D objects in Library of Congress. |

### Audio Recording

| Action | Method | Description |
| --- | --- | --- |
| [Search Audio Recordings](actions/search-audio-recordings.md) | GET | Finds audio recordings in Library of Congress. |

### Book

| Action | Method | Description |
| --- | --- | --- |
| [Search Books](actions/search-books.md) | GET | Finds books in Library of Congress. |

### Collection

| Action | Method | Description |
| --- | --- | --- |
| [Get Collection](actions/get-collection.md) | GET | Retrieves a Library of Congress digital collection. |
| [List Collections](actions/list-collections.md) | GET | Retrieves Library of Congress digital collections. |

### Collection Facets

| Action | Method | Description |
| --- | --- | --- |
| [Get Collection Facets](actions/get-collection-facets.md) | GET | Retrieves facets for a Library of Congress collection. |

### Collection Pagination

| Action | Method | Description |
| --- | --- | --- |
| [Get Collection Pagination](actions/get-collection-pagination.md) | GET | Retrieves pagination for a Library of Congress collection. |

### Film Or Video

| Action | Method | Description |
| --- | --- | --- |
| [Search Film and Videos](actions/search-film-and-videos.md) | GET | Finds films and videos in Library of Congress. |

### Item Citation

| Action | Method | Description |
| --- | --- | --- |
| [Get Item Citation](actions/get-item-citation.md) | GET | Retrieves citation formats for a Library of Congress item. |

### Item Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get Item Metadata](actions/get-item-metadata.md) | GET | Retrieves metadata for a Library of Congress item. |

### Item Resource

| Action | Method | Description |
| --- | --- | --- |
| [Get Item Resources](actions/get-item-resources.md) | GET | Retrieves resources for a Library of Congress item. |

### Library Item

| Action | Method | Description |
| --- | --- | --- |
| [Get Collection Results](actions/get-collection-results.md) | GET | Retrieves results from a Library of Congress collection. |
| [Get Item](actions/get-item.md) | GET | Retrieves a Library of Congress item. |
| [Search All Content](actions/search-all-content.md) | GET | Finds content across Library of Congress by keyword. |
| [Search Collection Items](actions/search-collection-items.md) | GET | Finds items in a Library of Congress collection. |

### Manuscript

| Action | Method | Description |
| --- | --- | --- |
| [Search Manuscripts](actions/search-manuscripts.md) | GET | Finds manuscripts in Library of Congress. |

### Map

| Action | Method | Description |
| --- | --- | --- |
| [Search Maps](actions/search-maps.md) | GET | Finds maps in Library of Congress. |

### Newspaper

| Action | Method | Description |
| --- | --- | --- |
| [Search Newspapers](actions/search-newspapers.md) | GET | Finds newspapers in Library of Congress. |

### Notated Music

| Action | Method | Description |
| --- | --- | --- |
| [Search Notated Music](actions/search-notated-music.md) | GET | Finds notated music in Library of Congress. |

### Periodical

| Action | Method | Description |
| --- | --- | --- |
| [Search Periodicals](actions/search-periodicals.md) | GET | Finds periodicals in Library of Congress. |

### Personal Narrative

| Action | Method | Description |
| --- | --- | --- |
| [Search Personal Narratives](actions/search-personal-narratives.md) | GET | Finds personal narratives in Library of Congress. |

### Photo Or Print

| Action | Method | Description |
| --- | --- | --- |
| [Search Photos](actions/search-photos.md) | GET | Finds photos, prints, and drawings in Library of Congress. |

### Related Resource

| Action | Method | Description |
| --- | --- | --- |
| [Get Resource Related Resources](actions/get-resource-related-resources.md) | GET | Retrieves related resources for a Library of Congress resource. |

### Resource

| Action | Method | Description |
| --- | --- | --- |
| [Get Resource](actions/get-resource.md) | GET | Retrieves a Library of Congress resource. |

### Resource Citation

| Action | Method | Description |
| --- | --- | --- |
| [Get Resource Citation](actions/get-resource-citation.md) | GET | Retrieves citation formats for a Library of Congress resource. |

### Resource Details

| Action | Method | Description |
| --- | --- | --- |
| [Get Resource Details](actions/get-resource-details.md) | GET | Retrieves details for a Library of Congress resource. |

### Resource Page

| Action | Method | Description |
| --- | --- | --- |
| [Get Resource Page](actions/get-resource-page.md) | GET | Retrieves page data for a Library of Congress resource. |

### Resource Segment

| Action | Method | Description |
| --- | --- | --- |
| [Get Resource Segments](actions/get-resource-segments.md) | GET | Retrieves segments for a Library of Congress resource. |

### Software Or E-resource

| Action | Method | Description |
| --- | --- | --- |
| [Search Software and E-Resources](actions/search-software-and-e-resources.md) | GET | Finds software and e-resources in Library of Congress. |

### Sound Recording

| Action | Method | Description |
| --- | --- | --- |
| [Search Sound Recordings](actions/search-sound-recordings.md) | GET | Finds sound recordings in Library of Congress. |

### Web Archive

| Action | Method | Description |
| --- | --- | --- |
| [Search Web Archives](actions/search-web-archives.md) | GET | Finds web archives in Library of Congress. |

