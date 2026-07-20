# <img src="https://images.mindcloud.co/apps/icons/logo-kis-marron-ovm-pcr0z_1775655798465.png" alt="KIS logo" width="28" height="28"> KIS: Universal API

Connect to KIS with an app token and secret, then list data tables and create, read, update, or delete records in KIS data tables.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/kIS/latest
- **Category:** IT Operations / Database
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://kis.work/
- **Vendor API docs:** https://doc.getkis.io/documentation/documentation-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Tables](actions/list-tables.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kIS/latest/actions/list-tables?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Sign In](actions/sign-in.md) | GET | Signs in to the KIS API. |

### Collections

| Action | Method | Description |
| --- | --- | --- |
| [List Tables](actions/list-tables.md) | GET | Retrieves all data table structures from KIS. |
| [Wipe Table](actions/wipe-table.md) | DELETE | Deletes all records from a KIS data table. |

### Custom Objects

| Action | Method | Description |
| --- | --- | --- |
| [Create Records](actions/create-records.md) | POST | Creates one or more records in a KIS data table. |
| [Delete Record](actions/delete-record.md) | DELETE | Deletes an existing record from a KIS data table. |
| [List Records](actions/list-records.md) | GET | Retrieves all records from a KIS data table. |
| [Update Record](actions/update-record.md) | PUT | Updates an existing record in a KIS data table. |

