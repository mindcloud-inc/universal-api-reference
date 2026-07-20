# Storyscale: Native API Reference

A consolidated summary of Storyscale's API configuration and 41 documented operations, with links to official documentation.

- **Official docs:** https://prodapi.storyscale.com/docs
- **OpenAPI specification:** https://prodapi.storyscale.com/docs
- **API base URL:** `https://prodapi.storyscale.com/api`

## Authentication

### Account Login

Sign in to Storyscale with email and password to obtain a bearer token for the main admin API.

### Credentials

- **Email:** `email` · required · Storyscale account email used for login.
- **Password:** `password` · required · Storyscale account password used for login.

Send these headers with each API request:

```http
Authorization: Bearer <custom.data.access_token>
```

[Official authentication documentation](https://prodapi.storyscale.com/docs)

## Endpoints (41 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Assets To Sequences](actions/add-assets-to-sequences.md) | `POST /v1/library/add-to-sequences` | [docs](https://prodapi.storyscale.com/docs) |
| [Add Sequence To Experience](actions/add-sequence-to-experience.md) | `POST /v1/experience/add-sequence/{id}` | [docs](https://prodapi.storyscale.com/docs) |
| [Clone Tour](actions/clone-tour.md) | `PUT /v1/tour/clone/{id}` | [docs](https://prodapi.storyscale.com/docs) |
| [Create Experience](actions/create-experience.md) | `POST /v1/experience/create` | [docs](https://prodapi.storyscale.com/docs) |
| [Create Library Asset](actions/create-library-asset.md) | `POST /v1/library/create` | [docs](https://prodapi.storyscale.com/docs) |
| [Create Sequence](actions/create-sequence.md) | `POST /v1/sequence/create` | [docs](https://prodapi.storyscale.com/docs) |
| [Create Style Guide](actions/create-style-guide.md) | `POST /v1/style-guide/create` | [docs](https://prodapi.storyscale.com/docs) |
| [Create Tour](actions/create-tour.md) | `POST /v1/tour/create/` | [docs](https://prodapi.storyscale.com/docs) |
| [Delete Experience](actions/delete-experience.md) | `DELETE /v1/experience/delete/{id}` | [docs](https://prodapi.storyscale.com/docs) |
| [Delete Library Asset](actions/delete-library-asset.md) | `DELETE /v1/library/delete/{id}` | [docs](https://prodapi.storyscale.com/docs) |
| [Delete Sequence](actions/delete-sequence.md) | `DELETE /v1/sequence/delete/{id}` | [docs](https://prodapi.storyscale.com/docs) |
| [Delete Style Guide](actions/delete-style-guide.md) | `DELETE /v1/style-guide/delete/{id}` | [docs](https://prodapi.storyscale.com/docs) |
| [Delete Tour](actions/delete-tour.md) | `DELETE /v1/tour/delete/{tour_id}` | [docs](https://prodapi.storyscale.com/docs) |
| [Get Access Token](actions/get-access-token.md) | `POST /v1/login` | [docs](https://prodapi.storyscale.com/docs) |
| [Get Experience](actions/get-experience.md) | `GET /v1/experience/view/{id}` | [docs](https://prodapi.storyscale.com/docs) |
| [Get Library Asset](actions/get-library-asset.md) | `GET /v1/library/view/{id}` | [docs](https://prodapi.storyscale.com/docs) |
| [Get Sequence](actions/get-sequence.md) | `GET /v1/sequence/view/{id}` | [docs](https://prodapi.storyscale.com/docs) |
| [Get Style Guide](actions/get-style-guide.md) | `GET /v1/style-guide/view/{id}` | [docs](https://prodapi.storyscale.com/docs) |
| [Get Tour](actions/get-tour.md) | `GET /v1/tour/view/{tour_id}/` | [docs](https://prodapi.storyscale.com/docs) |
| [List All Experiences](actions/list-all-experiences.md) | `GET /v1/experience/list-all` | [docs](https://prodapi.storyscale.com/docs) |
| [List All Sequences](actions/list-all-sequences.md) | `GET /v1/sequence/list` | [docs](https://prodapi.storyscale.com/docs) |
| [List Asset Types](actions/list-asset-types.md) | `GET /v1/library/asset-types` | [docs](https://prodapi.storyscale.com/docs) |
| [List Experience Types](actions/list-experience-types.md) | `GET /v1/experience/experience-types` | [docs](https://prodapi.storyscale.com/docs) |
| [List Experiences](actions/list-experiences.md) | `POST /v1/experience/show-all` | [docs](https://prodapi.storyscale.com/docs) |
| [List Experiences with Filters](actions/list-experiences-with-filters.md) | `POST /v1/experience/filterd/list-all` | [docs](https://prodapi.storyscale.com/docs) |
| [List Library Assets](actions/list-library-assets.md) | `POST /v1/library/show-all` | [docs](https://prodapi.storyscale.com/docs) |
| [List Platform Tags](actions/list-platform-tags.md) | `GET /v1/library/platform-tags` | [docs](https://prodapi.storyscale.com/docs) |
| [List Sequence Experiences](actions/list-sequence-experiences.md) | `GET /v1/sequence/experiences/{id}` | [docs](https://prodapi.storyscale.com/docs) |
| [List Sequences](actions/list-sequences.md) | `POST /v1/sequence/show-all` | [docs](https://prodapi.storyscale.com/docs) |
| [List Style Guides](actions/list-style-guides.md) | `GET /v1/style-guide/show-all` | [docs](https://prodapi.storyscale.com/docs) |
| [List Target Audience Segments](actions/list-target-audience-segments.md) | `GET /v1/experience/target-audience-segments` | [docs](https://prodapi.storyscale.com/docs) |
| [List Tours](actions/list-tours.md) | `GET /v1/tour/show-all` | [docs](https://prodapi.storyscale.com/docs) |
| [Publish Tour](actions/publish-tour.md) | `POST /v1/tour/publish/{id}` | [docs](https://prodapi.storyscale.com/docs) |
| [Search Experiences, Sequences, and Assets](actions/search-experiences-sequences-and-assets.md) | `GET /v1/search` | [docs](https://prodapi.storyscale.com/docs) |
| [Search Library Assets](actions/search-library-assets.md) | `GET /v1/library/search` | [docs](https://prodapi.storyscale.com/docs) |
| [Update Experience](actions/update-experience.md) | `PUT /v1/experience/update/{id}` | [docs](https://prodapi.storyscale.com/docs) |
| [Update Library Asset](actions/update-library-asset.md) | `PUT /v1/library/update/{id}` | [docs](https://prodapi.storyscale.com/docs) |
| [Update Library Asset Tags](actions/update-library-asset-tags.md) | `POST /v1/library/update-tags/{id}` | [docs](https://prodapi.storyscale.com/docs) |
| [Update Sequence](actions/update-sequence.md) | `PUT /v1/sequence/update/{id}` | [docs](https://prodapi.storyscale.com/docs) |
| [Update Style Guide](actions/update-style-guide.md) | `PUT /v1/style-guide/update/{id}` | [docs](https://prodapi.storyscale.com/docs) |
| [Update Tour](actions/update-tour.md) | `PUT /v1/tour/update/{id}` | [docs](https://prodapi.storyscale.com/docs) |
