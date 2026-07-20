# <img src="https://images.mindcloud.co/apps/icons/abbreviations-icon_1777655683668.png" alt="Abbreviations logo" width="28" height="28"> Abbreviations: Universal API

Search classified acronyms, abbreviations, and initialisms from Abbreviations.com using the STANDS4 Abbreviations API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/abbreviations/latest
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.abbreviations.com/
- **Vendor API docs:** https://www.abbreviations.com/abbr_api.php

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Lookup Abbreviation](actions/lookup-abbreviation.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/abbreviations/latest/actions/lookup-abbreviation?connectionId=$CONNECTION_ID&term=asap" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Abbreviation Result

| Action | Method | Description |
| --- | --- | --- |
| [Lookup Abbreviation](actions/lookup-abbreviation.md) | GET |  |
| [Reverse Lookup Abbreviation](actions/reverse-lookup-abbreviation.md) | GET |  |

