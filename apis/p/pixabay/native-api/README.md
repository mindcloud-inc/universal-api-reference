# Pixabay: Native API Reference

A consolidated summary of Pixabay's API configuration and 57 documented operations, with links to official documentation.

- **Official docs:** https://pixabay.com/api/docs/
- **API base URL:** `https://pixabay.com`

## Authentication

### API Key

Authenticate with a Pixabay API key sent in the shared key query parameter.

### Credentials

- **API Key:** `apiKey` · required · Your Pixabay API key.

[Official authentication documentation](https://pixabay.com/api/docs/)

## API conventions

Response data is read from `hits`.

## Pagination

Use `per_page` in the query string to set the page size (default 20; accepted range 3–200). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `order` in the query string. Only one sort field is accepted.

## Endpoints (57 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Image by ID](actions/get-image-by-id.md) | `GET /api/` | [docs](https://pixabay.com/api/docs/) |
| [Get Video by ID](actions/get-video-by-id.md) | `GET /api/videos/` | [docs](https://pixabay.com/api/docs/) |
| [Search Animal Images](actions/search-animal-images.md) | `GET /api/` | [docs](https://pixabay.com/api/docs/) |
| [Search Animal Videos](actions/search-animal-videos.md) | `GET /api/videos/` | [docs](https://pixabay.com/api/docs/) |
| [Search Animations](actions/search-animations.md) | `GET /api/videos/` | [docs](https://pixabay.com/api/docs/) |
| [Search Background Images](actions/search-background-images.md) | `GET /api/` | [docs](https://pixabay.com/api/docs/) |
| [Search Background Videos](actions/search-background-videos.md) | `GET /api/videos/` | [docs](https://pixabay.com/api/docs/) |
| [Search Building Images](actions/search-building-images.md) | `GET /api/` | [docs](https://pixabay.com/api/docs/) |
| [Search Building Videos](actions/search-building-videos.md) | `GET /api/videos/` | [docs](https://pixabay.com/api/docs/) |
| [Search Business Images](actions/search-business-images.md) | `GET /api/` | [docs](https://pixabay.com/api/docs/) |
| [Search Business Videos](actions/search-business-videos.md) | `GET /api/videos/` | [docs](https://pixabay.com/api/docs/) |
| [Search Computer Images](actions/search-computer-images.md) | `GET /api/` | [docs](https://pixabay.com/api/docs/) |
| [Search Computer Videos](actions/search-computer-videos.md) | `GET /api/videos/` | [docs](https://pixabay.com/api/docs/) |
| [Search Editor's Choice Images](actions/search-editors-choice-images.md) | `GET /api/` | [docs](https://pixabay.com/api/docs/) |
| [Search Editor's Choice Videos](actions/search-editors-choice-videos.md) | `GET /api/videos/` | [docs](https://pixabay.com/api/docs/) |
| [Search Education Images](actions/search-education-images.md) | `GET /api/` | [docs](https://pixabay.com/api/docs/) |
| [Search Education Videos](actions/search-education-videos.md) | `GET /api/videos/` | [docs](https://pixabay.com/api/docs/) |
| [Search Fashion Images](actions/search-fashion-images.md) | `GET /api/` | [docs](https://pixabay.com/api/docs/) |
| [Search Fashion Videos](actions/search-fashion-videos.md) | `GET /api/videos/` | [docs](https://pixabay.com/api/docs/) |
| [Search Feeling Images](actions/search-feeling-images.md) | `GET /api/` | [docs](https://pixabay.com/api/docs/) |
| [Search Feeling Videos](actions/search-feeling-videos.md) | `GET /api/videos/` | [docs](https://pixabay.com/api/docs/) |
| [Search Films](actions/search-films.md) | `GET /api/videos/` | [docs](https://pixabay.com/api/docs/) |
| [Search Food Images](actions/search-food-images.md) | `GET /api/` | [docs](https://pixabay.com/api/docs/) |
| [Search Food Videos](actions/search-food-videos.md) | `GET /api/videos/` | [docs](https://pixabay.com/api/docs/) |
| [Search Health Images](actions/search-health-images.md) | `GET /api/` | [docs](https://pixabay.com/api/docs/) |
| [Search Health Videos](actions/search-health-videos.md) | `GET /api/videos/` | [docs](https://pixabay.com/api/docs/) |
| [Search Horizontal Images](actions/search-horizontal-images.md) | `GET /api/` | [docs](https://pixabay.com/api/docs/) |
| [Search Illustrations](actions/search-illustrations.md) | `GET /api/` | [docs](https://pixabay.com/api/docs/) |
| [Search Images](actions/search-images.md) | `GET /api/` | [docs](https://pixabay.com/api/docs/) |
| [Search Industry Images](actions/search-industry-images.md) | `GET /api/` | [docs](https://pixabay.com/api/docs/) |
| [Search Industry Videos](actions/search-industry-videos.md) | `GET /api/videos/` | [docs](https://pixabay.com/api/docs/) |
| [Search Latest Images](actions/search-latest-images.md) | `GET /api/` | [docs](https://pixabay.com/api/docs/) |
| [Search Latest Videos](actions/search-latest-videos.md) | `GET /api/videos/` | [docs](https://pixabay.com/api/docs/) |
| [Search Music Images](actions/search-music-images.md) | `GET /api/` | [docs](https://pixabay.com/api/docs/) |
| [Search Music Videos](actions/search-music-videos.md) | `GET /api/videos/` | [docs](https://pixabay.com/api/docs/) |
| [Search Nature Images](actions/search-nature-images.md) | `GET /api/` | [docs](https://pixabay.com/api/docs/) |
| [Search Nature Videos](actions/search-nature-videos.md) | `GET /api/videos/` | [docs](https://pixabay.com/api/docs/) |
| [Search People Images](actions/search-people-images.md) | `GET /api/` | [docs](https://pixabay.com/api/docs/) |
| [Search People Videos](actions/search-people-videos.md) | `GET /api/videos/` | [docs](https://pixabay.com/api/docs/) |
| [Search Photos](actions/search-photos.md) | `GET /api/` | [docs](https://pixabay.com/api/docs/) |
| [Search Place Images](actions/search-place-images.md) | `GET /api/` | [docs](https://pixabay.com/api/docs/) |
| [Search Place Videos](actions/search-place-videos.md) | `GET /api/videos/` | [docs](https://pixabay.com/api/docs/) |
| [Search Religion Images](actions/search-religion-images.md) | `GET /api/` | [docs](https://pixabay.com/api/docs/) |
| [Search Religion Videos](actions/search-religion-videos.md) | `GET /api/videos/` | [docs](https://pixabay.com/api/docs/) |
| [Search Safe Images](actions/search-safe-images.md) | `GET /api/` | [docs](https://pixabay.com/api/docs/) |
| [Search Safe Videos](actions/search-safe-videos.md) | `GET /api/videos/` | [docs](https://pixabay.com/api/docs/) |
| [Search Science Images](actions/search-science-images.md) | `GET /api/` | [docs](https://pixabay.com/api/docs/) |
| [Search Science Videos](actions/search-science-videos.md) | `GET /api/videos/` | [docs](https://pixabay.com/api/docs/) |
| [Search Sports Images](actions/search-sports-images.md) | `GET /api/` | [docs](https://pixabay.com/api/docs/) |
| [Search Sports Videos](actions/search-sports-videos.md) | `GET /api/videos/` | [docs](https://pixabay.com/api/docs/) |
| [Search Transportation Images](actions/search-transportation-images.md) | `GET /api/` | [docs](https://pixabay.com/api/docs/) |
| [Search Transportation Videos](actions/search-transportation-videos.md) | `GET /api/videos/` | [docs](https://pixabay.com/api/docs/) |
| [Search Travel Images](actions/search-travel-images.md) | `GET /api/` | [docs](https://pixabay.com/api/docs/) |
| [Search Travel Videos](actions/search-travel-videos.md) | `GET /api/videos/` | [docs](https://pixabay.com/api/docs/) |
| [Search Vectors](actions/search-vectors.md) | `GET /api/` | [docs](https://pixabay.com/api/docs/) |
| [Search Vertical Images](actions/search-vertical-images.md) | `GET /api/` | [docs](https://pixabay.com/api/docs/) |
| [Search Videos](actions/search-videos.md) | `GET /api/videos/` | [docs](https://pixabay.com/api/docs/) |
