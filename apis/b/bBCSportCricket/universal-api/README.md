# <img src="https://images.mindcloud.co/apps/icons/b-bcsport-cricket_1776361473747.png" alt="BBC Sport - Cricket logo" width="28" height="28"> BBC Sport - Cricket: Universal API

Read BBC Sport cricket headlines and score updates

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bBCSportCricket/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.bbc.co.uk/sport/cricket
- **Vendor API docs:** https://feeds.bbci.co.uk/sport/cricket/rss.xml

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Cricket Headlines](actions/list-cricket-headlines.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bBCSportCricket/latest/actions/list-cricket-headlines?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Announcements

| Action | Method | Description |
| --- | --- | --- |
| [List Afghanistan Cricket Headlines](actions/list-afghanistan-cricket-headlines.md) | GET | Retrieves BBC Sport Afghanistan cricket headlines. |
| [List Australia Cricket Headlines](actions/list-australia-cricket-headlines.md) | GET | Retrieves BBC Sport Australia cricket headlines. |
| [List Bangladesh Cricket Headlines](actions/list-bangladesh-cricket-headlines.md) | GET | Retrieves BBC Sport Bangladesh cricket headlines. |
| [List County Cricket Headlines](actions/list-county-cricket-headlines.md) | GET | Retrieves BBC Sport county cricket headlines. |
| [List Cricket Headlines](actions/list-cricket-headlines.md) | GET | Retrieves latest BBC Sport cricket headlines. |
| [List England Cricket Headlines](actions/list-england-cricket-headlines.md) | GET | Retrieves BBC Sport England cricket headlines. |
| [List England Women Cricket Headlines](actions/list-england-women-cricket-headlines.md) | GET | Retrieves BBC Sport England women's cricket headlines. |
| [List Franchise Cricket Headlines](actions/list-franchise-cricket-headlines.md) | GET | Retrieves BBC Sport franchise cricket headlines. |
| [List India Cricket Headlines](actions/list-india-cricket-headlines.md) | GET | Retrieves BBC Sport India cricket headlines. |
| [List Ireland Cricket Headlines](actions/list-ireland-cricket-headlines.md) | GET | Retrieves BBC Sport Ireland cricket headlines. |
| [List New Zealand Cricket Headlines](actions/list-new-zealand-cricket-headlines.md) | GET | Retrieves BBC Sport New Zealand cricket headlines. |
| [List Pakistan Cricket Headlines](actions/list-pakistan-cricket-headlines.md) | GET | Retrieves BBC Sport Pakistan cricket headlines. |
| [List Scotland Cricket Headlines](actions/list-scotland-cricket-headlines.md) | GET | Retrieves BBC Sport Scotland cricket headlines. |
| [List South Africa Cricket Headlines](actions/list-south-africa-cricket-headlines.md) | GET | Retrieves BBC Sport South Africa cricket headlines. |
| [List Sri Lanka Cricket Headlines](actions/list-sri-lanka-cricket-headlines.md) | GET | Retrieves BBC Sport Sri Lanka cricket headlines. |
| [List Surrey Cricket Headlines](actions/list-surrey-cricket-headlines.md) | GET | Retrieves BBC Sport Surrey cricket headlines. |
| [List The Hundred Headlines](actions/list-the-hundred-headlines.md) | GET | Retrieves BBC Sport The Hundred cricket headlines. |
| [List West Indies Cricket Headlines](actions/list-west-indies-cricket-headlines.md) | GET | Retrieves BBC Sport West Indies cricket headlines. |
| [List Yorkshire Cricket Headlines](actions/list-yorkshire-cricket-headlines.md) | GET | Retrieves BBC Sport Yorkshire cricket headlines. |
| [List Zimbabwe Cricket Headlines](actions/list-zimbabwe-cricket-headlines.md) | GET | Retrieves BBC Sport Zimbabwe cricket headlines. |

