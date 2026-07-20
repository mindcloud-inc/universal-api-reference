# <img src="https://images.mindcloud.co/apps/icons/favicon-16x16_1776269556293.png" alt="Dungeon Fighter Online logo" width="28" height="28"> Dungeon Fighter Online: Universal API

Dungeon Fighter Online is a multiplayer action RPG. This MindCloud app wraps Neople Developers' Dungeon & Fighter Open API for read-only game metadata such as server, character, auction, item, and job information.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dungeonFighterOnline/latest
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.dfoneople.com/
- **Vendor API docs:** https://developers.neople.co.kr/contents/apiDocs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Servers](actions/list-servers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dungeonFighterOnline/latest/actions/list-servers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Auction Item

| Action | Method | Description |
| --- | --- | --- |
| [Get Auction Item](actions/get-auction-item.md) | GET | Retrieves an auction listing from Dungeon Fighter Online. |
| [Search Auction Items](actions/search-auction-items.md) | GET | Finds auction listings in Dungeon Fighter Online by item name. |

### Avatar Market Hashtag

| Action | Method | Description |
| --- | --- | --- |
| [List Avatar Market Hashtags](actions/list-avatar-market-hashtags.md) | GET | Retrieves avatar market hashtags from Dungeon Fighter Online. |

### Avatar Market Sale

| Action | Method | Description |
| --- | --- | --- |
| [Get Avatar Market Sale](actions/get-avatar-market-sale.md) | GET | Retrieves an avatar market listing from Dungeon Fighter Online. |
| [Search Avatar Market Sales](actions/search-avatar-market-sales.md) | GET | Finds avatar market listings in Dungeon Fighter Online. |

### Item

| Action | Method | Description |
| --- | --- | --- |
| [Get Item](actions/get-item.md) | GET | Retrieves item details from Dungeon Fighter Online. |
| [Get Multiple Items](actions/get-multiple-items.md) | GET | Retrieves details for multiple items from Dungeon Fighter Online. |
| [Search Items](actions/search-items.md) | GET | Finds items in Dungeon Fighter Online by item name. |

### Item Hashtag

| Action | Method | Description |
| --- | --- | --- |
| [List Item Hashtags](actions/list-item-hashtags.md) | GET | Retrieves item hashtags from Dungeon Fighter Online. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [List Jobs](actions/list-jobs.md) | GET | Retrieves job information from Dungeon Fighter Online. |

### Server

| Action | Method | Description |
| --- | --- | --- |
| [List Servers](actions/list-servers.md) | GET | Retrieves server information from Dungeon Fighter Online. |

### Set Item

| Action | Method | Description |
| --- | --- | --- |
| [Get Multiple Set Items](actions/get-multiple-set-items.md) | GET | Retrieves details for multiple set items from Dungeon Fighter Online. |
| [Get Set Item](actions/get-set-item.md) | GET | Retrieves set item details from Dungeon Fighter Online. |
| [Search Set Items](actions/search-set-items.md) | GET | Finds set items in Dungeon Fighter Online by set name. |

### Skill

| Action | Method | Description |
| --- | --- | --- |
| [Get Multiple Skills](actions/get-multiple-skills.md) | GET | Retrieves details for multiple skills from Dungeon Fighter Online. |
| [Get Skill](actions/get-skill.md) | GET | Retrieves skill details from Dungeon Fighter Online. |
| [List Skills](actions/list-skills.md) | GET | Retrieves a job's skills from Dungeon Fighter Online. |

### Sold Auction Item

| Action | Method | Description |
| --- | --- | --- |
| [Search Sold Auction Items](actions/search-sold-auction-items.md) | GET | Finds sold auction listings in Dungeon Fighter Online by item name. |

### Sold Avatar Market Item

| Action | Method | Description |
| --- | --- | --- |
| [Get Avatar Market Sold Item](actions/get-avatar-market-sold-item.md) | GET | Retrieves sold avatar market pricing from Dungeon Fighter Online. |
| [Search Avatar Market Sold Items](actions/search-avatar-market-sold-items.md) | GET | Finds sold avatar market listings in Dungeon Fighter Online. |

