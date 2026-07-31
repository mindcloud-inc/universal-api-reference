# Ice and Fire (Game of Thrones): Native API Reference

A consolidated summary of Ice and Fire (Game of Thrones)'s API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://github.com/joakimskoog/AnApiOfIceAndFire/wiki
- **API base URL:** `https://anapioficeandfire.com/api`

## Authentication

### Public API

This API is public and does not require credentials.

This API does not require request authentication.

[Official authentication documentation](https://github.com/joakimskoog/AnApiOfIceAndFire/wiki/Authentication)

## Pagination

Use `pageSize` in the query string to set the page size (default 10; maximum 50). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Book](actions/get-book.md) | `GET /books/:bookId` | [docs](https://github.com/joakimskoog/AnApiOfIceAndFire/wiki/Books) |
| [Get Character](actions/get-character.md) | `GET /characters/:characterId` | [docs](https://github.com/joakimskoog/AnApiOfIceAndFire/wiki/Characters) |
| [Get House](actions/get-house.md) | `GET /houses/:houseId` | [docs](https://github.com/joakimskoog/AnApiOfIceAndFire/wiki/Houses) |
| [List Books](actions/list-books.md) | `GET /books` | [docs](https://github.com/joakimskoog/AnApiOfIceAndFire/wiki/Books) |
| [List Characters](actions/list-characters.md) | `GET /characters` | [docs](https://github.com/joakimskoog/AnApiOfIceAndFire/wiki/Characters) |
| [List Houses](actions/list-houses.md) | `GET /houses` | [docs](https://github.com/joakimskoog/AnApiOfIceAndFire/wiki/Houses) |
