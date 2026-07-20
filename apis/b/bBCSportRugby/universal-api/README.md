# <img src="https://images.mindcloud.co/apps/icons/b-bcsport-rugby_1776361484035.png" alt="BBC Sport - Rugby logo" width="28" height="28"> BBC Sport - Rugby: Universal API

Read BBC Sport rugby headlines and article links

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/bBCSportRugby/latest
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.bbc.co.uk/sport
- **Vendor API docs:** https://support.bbc.co.uk/platform/feeds/SportFeeds.htm

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Bath Rugby Headlines](actions/list-bath-rugby-headlines.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bBCSportRugby/latest/actions/list-bath-rugby-headlines?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Rugby Headline

| Action | Method | Description |
| --- | --- | --- |
| [List Bath Rugby Headlines](actions/list-bath-rugby-headlines.md) | GET | Retrieves Bath rugby headlines from BBC Sport - Rugby. |
| [List Bristol Rugby Headlines](actions/list-bristol-rugby-headlines.md) | GET | Retrieves Bristol rugby headlines from BBC Sport - Rugby. |
| [List Edinburgh Rugby Headlines](actions/list-edinburgh-rugby-headlines.md) | GET | Retrieves Edinburgh rugby headlines from BBC Sport - Rugby. |
| [List England Rugby Team Headlines](actions/list-england-rugby-team-headlines.md) | GET | Retrieves England rugby team headlines from BBC Sport - Rugby. |
| [List English Rugby Headlines](actions/list-english-rugby-headlines.md) | GET | Retrieves English rugby headlines from BBC Sport - Rugby. |
| [List Harlequins Rugby Headlines](actions/list-harlequins-rugby-headlines.md) | GET | Retrieves Harlequins rugby headlines from BBC Sport - Rugby. |
| [List Hull KR Headlines](actions/list-hull-kr-headlines.md) | GET | Retrieves Hull KR headlines from BBC Sport - Rugby. |
| [List Ireland Rugby Team Headlines](actions/list-ireland-rugby-team-headlines.md) | GET | Retrieves Ireland rugby team headlines from BBC Sport - Rugby. |
| [List Irish Rugby Headlines](actions/list-irish-rugby-headlines.md) | GET | Retrieves Irish rugby headlines from BBC Sport - Rugby. |
| [List Leicester Rugby Headlines](actions/list-leicester-rugby-headlines.md) | GET | Retrieves Leicester rugby headlines from BBC Sport - Rugby. |
| [List Leinster Rugby Headlines](actions/list-leinster-rugby-headlines.md) | GET | Retrieves Leinster rugby headlines from BBC Sport - Rugby. |
| [List Munster Rugby Headlines](actions/list-munster-rugby-headlines.md) | GET | Retrieves Munster rugby headlines from BBC Sport - Rugby. |
| [List Rugby League Headlines](actions/list-rugby-league-headlines.md) | GET | Retrieves rugby league headlines from BBC Sport - Rugby. |
| [List Rugby Union Headlines](actions/list-rugby-union-headlines.md) | GET | Retrieves rugby union headlines from BBC Sport - Rugby. |
| [List Scotland Rugby Team Headlines](actions/list-scotland-rugby-team-headlines.md) | GET | Retrieves Scotland rugby team headlines from BBC Sport - Rugby. |
| [List Scottish Rugby Headlines](actions/list-scottish-rugby-headlines.md) | GET | Retrieves Scottish rugby headlines from BBC Sport - Rugby. |
| [List St Helens Headlines](actions/list-st-helens-headlines.md) | GET | Retrieves St Helens headlines from BBC Sport - Rugby. |
| [List Ulster Rugby Headlines](actions/list-ulster-rugby-headlines.md) | GET | Retrieves Ulster rugby headlines from BBC Sport - Rugby. |
| [List Wales Rugby Team Headlines](actions/list-wales-rugby-team-headlines.md) | GET | Retrieves Wales rugby team headlines from BBC Sport - Rugby. |
| [List Welsh Rugby Headlines](actions/list-welsh-rugby-headlines.md) | GET | Retrieves Welsh rugby headlines from BBC Sport - Rugby. |

