# <img src="https://images.mindcloud.co/apps/icons/d-d5e_1785420682653.png" alt="D&D 5e logo" width="28" height="28"> D&D 5e: Universal API

D&D 5e through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dD5e/latest
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Class](actions/get-classe.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dD5e/latest/actions/get-classe?connectionId=$CONNECTION_ID&index=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Classe

| Action | Method | Description |
| --- | --- | --- |
| [Get Class](actions/get-classe.md) | GET |  |
| [List Classes](actions/list-classes.md) | GET |  |

### Condition

| Action | Method | Description |
| --- | --- | --- |
| [Get Condition](actions/get-condition.md) | GET |  |
| [List Conditions](actions/list-conditions.md) | GET |  |

### Equipmen

| Action | Method | Description |
| --- | --- | --- |
| [Get Equipment](actions/get-equipmen.md) | GET |  |
| [List Equipment](actions/list-equipment.md) | GET |  |

### Monster

| Action | Method | Description |
| --- | --- | --- |
| [Get Monster](actions/get-monster.md) | GET |  |
| [List Monsters](actions/list-monsters.md) | GET |  |

### Race

| Action | Method | Description |
| --- | --- | --- |
| [Get Race](actions/get-race.md) | GET |  |
| [List Races](actions/list-races.md) | GET |  |

### Resource Index

| Action | Method | Description |
| --- | --- | --- |
| [Get Resource Index](actions/get-resource-index.md) | GET |  |

### Spell

| Action | Method | Description |
| --- | --- | --- |
| [Get Spell](actions/get-spell.md) | GET |  |
| [List Spells](actions/list-spells.md) | GET |  |

