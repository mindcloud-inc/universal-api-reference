# <img src="https://images.mindcloud.co/apps/icons/harry-potter_1775755826512.png" alt="Harry Potter logo" width="28" height="28"> Harry Potter: Universal API

Public Harry Potter API with character, house, student, staff, and spell lookup actions.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/harryPotter/latest
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://hp-api.onrender.com/
- **Vendor API docs:** https://hp-api.onrender.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Character By ID](actions/get-character-by-id.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harryPotter/latest/actions/get-character-by-id?connectionId=$CONNECTION_ID&id=e.g.%209e3f7ce4-b9a7-4244-b709-dae5c1f1d4a8" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Character

| Action | Method | Description |
| --- | --- | --- |
| [Get Character By ID](actions/get-character-by-id.md) | GET | Retrieves a Harry Potter character by ID. |
| [List Characters](actions/list-characters.md) | GET | Retrieves Harry Potter characters. |
| [List Characters By House](actions/list-characters-by-house.md) | GET | Retrieves Harry Potter characters by Hogwarts house. |
| [List Staff](actions/list-staff.md) | GET | Retrieves Harry Potter staff characters. |
| [List Students](actions/list-students.md) | GET | Retrieves Harry Potter student characters. |

### Spell

| Action | Method | Description |
| --- | --- | --- |
| [List Spells](actions/list-spells.md) | GET | Retrieves Harry Potter spells. |

