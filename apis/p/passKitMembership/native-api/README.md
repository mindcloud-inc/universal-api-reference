# PassKit Membership: Native API Reference

A consolidated summary of PassKit Membership's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://docs.passkit.io/protocols/member/
- **API base URL:** `https://api.pub2.passkit.io`

## Authentication

### Long-Lived API Token

Use a PassKit long-lived API token for REST API requests. PassKit expects the token in the Authorization header with a Bearer prefix.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.passkit.com/en/articles/5743688-using-long-lived-api-tokens)

## Pagination

Use `limit` in the request body to set the page size (default 100; accepted range 1–1000). Use `offset` in the request body as the record offset; numbering starts at 0.

## Filtering

Send filters in the request body.

## Sorting

Set the sort field with `orderBy` in the request body. Set the direction separately with `orderAsc`. Use `true` for ascending order and `false` for descending order. Only one sort field is accepted.

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Count Members](actions/count-members.md) | `POST /members/count/:programId` | [docs](https://help.passkit.com/en/articles/4133757-membership-protocol-filtering-listing-and-counting-by-api) |
| [Count Members By External ID](actions/count-members-by-external-id.md) | `POST /members/count/:programId` | [docs](https://help.passkit.com/en/articles/4133757-membership-protocol-filtering-listing-and-counting-by-api) |
| [Create Member](actions/create-member.md) | `POST /members/member` | [docs](https://docs.passkit.io/protocols/member/) |
| [Delete Member](actions/delete-member.md) | `DELETE /members/member` | [docs](https://help.passkit.com/en/articles/4134575-editing-members-through-the-api) |
| [Find Member By External ID](actions/find-member-by-external-id.md) | `POST /members/member/list/:programId` | [docs](https://help.passkit.com/en/articles/4133757-membership-protocol-filtering-listing-and-counting-by-api) |
| [Get Member By External ID](actions/get-member-by-external-id.md) | `GET /members/member/externalId/:programId/:externalId` | [docs](https://docs.passkit.io/protocols/member/) |
| [List Members](actions/list-members.md) | `POST /members/member/list/:programId` | [docs](https://help.passkit.com/en/articles/4133757-membership-protocol-filtering-listing-and-counting-by-api) |
| [List Programs](actions/list-programs.md) | `POST /members/programs/list` | [docs](https://help.passkit.com/en/articles/4133757-membership-protocol-filtering-listing-and-counting-by-api) |
| [List Tiers](actions/list-tiers.md) | `POST /members/tiers/list` | [docs](https://help.passkit.com/en/articles/4133757-membership-protocol-filtering-listing-and-counting-by-api) |
| [Set Member Points By External ID](actions/set-member-points-by-external-id.md) | `PUT /members/member` | [docs](https://help.passkit.com/en/articles/4134575-editing-members-through-the-api) |
| [Set Member Secondary Points By External ID](actions/set-member-secondary-points-by-external-id.md) | `PUT /members/member` | [docs](https://help.passkit.com/en/articles/4134575-editing-members-through-the-api) |
| [Set Member Tier Points By External ID](actions/set-member-tier-points-by-external-id.md) | `PUT /members/member` | [docs](https://help.passkit.com/en/articles/4134575-editing-members-through-the-api) |
| [Update Member](actions/update-member.md) | `PUT /members/member` | [docs](https://help.passkit.com/en/articles/4134575-editing-members-through-the-api) |
| [Update Member By External ID](actions/update-member-by-external-id.md) | `PUT /members/member` | [docs](https://help.passkit.com/en/articles/4134575-editing-members-through-the-api) |
