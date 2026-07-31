# <img src="https://images.mindcloud.co/apps/icons/harry-potter-api_1785420663284.png" alt="Harry Potter API logo" width="28" height="28"> Harry Potter API: Universal API

Get Harry Potter characters and spells

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/harryPotterAPI/latest
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor API docs:** https://hp-api.onrender.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Character](actions/get-character.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harryPotterAPI/latest/actions/get-character?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Character

| Action | Method | Description |
| --- | --- | --- |
| [Get Character](actions/get-character.md) | GET |  |
| [List Characters](actions/list-characters.md) | GET |  |
| [List Characters by House](actions/list-characters-by-house.md) | GET |  |
| [List Staff](actions/list-staff.md) | GET |  |
| [List Students](actions/list-students.md) | GET |  |

### Spell

| Action | Method | Description |
| --- | --- | --- |
| [List Spells](actions/list-spells.md) | GET |  |

