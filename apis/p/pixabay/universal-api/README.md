# <img src="https://images.mindcloud.co/apps/icons/pixabay_1776102927953.png" alt="Pixabay logo" width="28" height="28"> Pixabay: Universal API

Pixabay provides a REST API for searching and retrieving royalty-free images and videos from the Pixabay media library.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pixabay/latest
- **Actions:** 57
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pixabay.com/
- **Vendor API docs:** https://pixabay.com/api/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Images](actions/search-images.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixabay/latest/actions/search-images?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (57)

### Image

| Action | Method | Description |
| --- | --- | --- |
| [Get Image by ID](actions/get-image-by-id.md) | GET | Finds an image in Pixabay by ID. |
| [Search Animal Images](actions/search-animal-images.md) | GET | Finds animal images in Pixabay. |
| [Search Background Images](actions/search-background-images.md) | GET | Finds background images in Pixabay. |
| [Search Building Images](actions/search-building-images.md) | GET | Finds building images in Pixabay. |
| [Search Business Images](actions/search-business-images.md) | GET | Finds business images in Pixabay. |
| [Search Computer Images](actions/search-computer-images.md) | GET | Finds computer images in Pixabay. |
| [Search Editor's Choice Images](actions/search-editors-choice-images.md) | GET | Finds editor's choice images in Pixabay. |
| [Search Education Images](actions/search-education-images.md) | GET | Finds education images in Pixabay. |
| [Search Fashion Images](actions/search-fashion-images.md) | GET | Finds fashion images in Pixabay. |
| [Search Feeling Images](actions/search-feeling-images.md) | GET | Finds images about feelings in Pixabay. |
| [Search Food Images](actions/search-food-images.md) | GET | Finds food images in Pixabay. |
| [Search Health Images](actions/search-health-images.md) | GET | Finds health images in Pixabay. |
| [Search Horizontal Images](actions/search-horizontal-images.md) | GET | Finds horizontal images in Pixabay. |
| [Search Illustrations](actions/search-illustrations.md) | GET | Finds illustrations in Pixabay. |
| [Search Images](actions/search-images.md) | GET | Finds images in Pixabay. |
| [Search Industry Images](actions/search-industry-images.md) | GET | Finds industry images in Pixabay. |
| [Search Latest Images](actions/search-latest-images.md) | GET | Finds the latest images in Pixabay. |
| [Search Music Images](actions/search-music-images.md) | GET | Finds music images in Pixabay. |
| [Search Nature Images](actions/search-nature-images.md) | GET | Finds nature images in Pixabay. |
| [Search People Images](actions/search-people-images.md) | GET | Finds people images in Pixabay. |
| [Search Photos](actions/search-photos.md) | GET | Finds photos in Pixabay. |
| [Search Place Images](actions/search-place-images.md) | GET | Finds images of places in Pixabay. |
| [Search Religion Images](actions/search-religion-images.md) | GET | Finds religion images in Pixabay. |
| [Search Safe Images](actions/search-safe-images.md) | GET | Finds safe images in Pixabay. |
| [Search Science Images](actions/search-science-images.md) | GET | Finds science images in Pixabay. |
| [Search Sports Images](actions/search-sports-images.md) | GET | Finds sports images in Pixabay. |
| [Search Transportation Images](actions/search-transportation-images.md) | GET | Finds transportation images in Pixabay. |
| [Search Travel Images](actions/search-travel-images.md) | GET | Finds travel images in Pixabay. |
| [Search Vectors](actions/search-vectors.md) | GET | Finds vector images in Pixabay. |
| [Search Vertical Images](actions/search-vertical-images.md) | GET | Finds vertical images in Pixabay. |

### Video

| Action | Method | Description |
| --- | --- | --- |
| [Get Video by ID](actions/get-video-by-id.md) | GET | Finds a video in Pixabay by ID. |
| [Search Animal Videos](actions/search-animal-videos.md) | GET | Finds animal videos in Pixabay. |
| [Search Animations](actions/search-animations.md) | GET | Finds animations in Pixabay. |
| [Search Background Videos](actions/search-background-videos.md) | GET | Finds background videos in Pixabay. |
| [Search Building Videos](actions/search-building-videos.md) | GET | Finds building videos in Pixabay. |
| [Search Business Videos](actions/search-business-videos.md) | GET | Finds business videos in Pixabay. |
| [Search Computer Videos](actions/search-computer-videos.md) | GET | Finds computer videos in Pixabay. |
| [Search Editor's Choice Videos](actions/search-editors-choice-videos.md) | GET | Finds editor's choice videos in Pixabay. |
| [Search Education Videos](actions/search-education-videos.md) | GET | Finds education videos in Pixabay. |
| [Search Fashion Videos](actions/search-fashion-videos.md) | GET | Finds fashion videos in Pixabay. |
| [Search Feeling Videos](actions/search-feeling-videos.md) | GET | Finds videos about feelings in Pixabay. |
| [Search Films](actions/search-films.md) | GET | Finds films in Pixabay. |
| [Search Food Videos](actions/search-food-videos.md) | GET | Finds food videos in Pixabay. |
| [Search Health Videos](actions/search-health-videos.md) | GET | Finds health videos in Pixabay. |
| [Search Industry Videos](actions/search-industry-videos.md) | GET | Finds industry videos in Pixabay. |
| [Search Latest Videos](actions/search-latest-videos.md) | GET | Finds the latest videos in Pixabay. |
| [Search Music Videos](actions/search-music-videos.md) | GET | Finds music videos in Pixabay. |
| [Search Nature Videos](actions/search-nature-videos.md) | GET | Finds nature videos in Pixabay. |
| [Search People Videos](actions/search-people-videos.md) | GET | Finds people videos in Pixabay. |
| [Search Place Videos](actions/search-place-videos.md) | GET | Finds videos of places in Pixabay. |
| [Search Religion Videos](actions/search-religion-videos.md) | GET | Finds religion videos in Pixabay. |
| [Search Safe Videos](actions/search-safe-videos.md) | GET | Finds safe videos in Pixabay. |
| [Search Science Videos](actions/search-science-videos.md) | GET | Finds science videos in Pixabay. |
| [Search Sports Videos](actions/search-sports-videos.md) | GET | Finds sports videos in Pixabay. |
| [Search Transportation Videos](actions/search-transportation-videos.md) | GET | Finds transportation videos in Pixabay. |
| [Search Travel Videos](actions/search-travel-videos.md) | GET | Finds travel videos in Pixabay. |
| [Search Videos](actions/search-videos.md) | GET | Finds videos in Pixabay. |

