# <img src="https://images.mindcloud.co/apps/icons/ice-and-fire-game-of-thrones_1785383232776.png" alt="Ice and Fire (Game of Thrones) logo" width="28" height="28"> Ice and Fire (Game of Thrones): Universal API

Explore Ice and Fire books, characters, and houses

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/iceAndFireGameOfThrones/latest
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://anapioficeandfire.com/
- **Vendor API docs:** https://github.com/joakimskoog/AnApiOfIceAndFire/wiki

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Book](actions/get-book.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iceAndFireGameOfThrones/latest/actions/get-book?connectionId=$CONNECTION_ID&bookId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Book

| Action | Method | Description |
| --- | --- | --- |
| [Get Book](actions/get-book.md) | GET |  |
| [List Books](actions/list-books.md) | GET |  |

### Character

| Action | Method | Description |
| --- | --- | --- |
| [Get Character](actions/get-character.md) | GET |  |
| [List Characters](actions/list-characters.md) | GET |  |

### House

| Action | Method | Description |
| --- | --- | --- |
| [Get House](actions/get-house.md) | GET |  |
| [List Houses](actions/list-houses.md) | GET |  |

