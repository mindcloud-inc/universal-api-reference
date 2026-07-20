# <img src="https://images.mindcloud.co/apps/icons/megaplan-icon_1776867119470.png" alt="Megaplan logo" width="28" height="28"> Megaplan: Universal API

Megaplan API v3 integration for CRM, tasks, employees, documents, offers, invoices, projects, and related account resources.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/megaplan/latest
- **Actions:** 60
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://megaplan.ru
- **Vendor API docs:** https://m60888876.megaplan.ru/api/v3/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Account Info](actions/get-account-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/megaplan/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (60)

### Account Info

| Action | Method | Description |
| --- | --- | --- |
| [List Account Info](actions/get-account-info.md) | GET |  |

### Consignment

| Action | Method | Description |
| --- | --- | --- |
| [Get Consignment](actions/g-et-consignment-id89c79c96.md) | GET |  |
| [List Consignment](actions/g-et-consignment8475e2fc.md) | GET |  |
| [Create Consignment](actions/p-ost-consignment-ide28969a6.md) | POST |  |

### Contractor Company

| Action | Method | Description |
| --- | --- | --- |
| [Delete Contractor Company](actions/d-elete-contractor-company-idf1fb1f9b.md) | DELETE |  |
| [Get Contractor Company](actions/g-et-contractor-company-idd2a96eab.md) | GET |  |
| [List Contractor Company](actions/g-et-contractor-company9e68924f.md) | GET |  |
| [Create Contractor Company](actions/p-ost-contractor-company-idf0ed4ae2.md) | POST |  |
| [Create Contractor Company](actions/p-ost-contractor-company6a39dd15.md) | POST |  |

### Contractor Human

| Action | Method | Description |
| --- | --- | --- |
| [Delete Contractor Human](actions/d-elete-contractor-human-idc1874191.md) | DELETE |  |
| [Get Contractor Human](actions/g-et-contractor-human-id161a9507.md) | GET |  |
| [List Contractor Human](actions/g-et-contractor-human1cb34131.md) | GET |  |
| [Create Contractor Human](actions/p-ost-contractor-human-id6294d755.md) | POST |  |
| [Create Contractor Human](actions/p-ost-contractor-human44f33981.md) | POST |  |

### Deal

| Action | Method | Description |
| --- | --- | --- |
| [Delete Deal](actions/d-elete-deal-id25a61849.md) | DELETE |  |
| [Get Deal](actions/g-et-deal-ida67919a2.md) | GET |  |
| [List Deal](actions/g-et-deal502406fe.md) | GET |  |
| [Create Deal](actions/p-ost-deal-id44864281.md) | POST |  |
| [Create Deal](actions/p-ost-dealff9859b3.md) | POST |  |

### Doc

| Action | Method | Description |
| --- | --- | --- |
| [Delete Doc](actions/d-elete-doc-ideef30a90.md) | DELETE |  |
| [Get Doc](actions/g-et-doc-id824f6a06.md) | GET |  |
| [List Doc](actions/g-et-doc34f3e930.md) | GET |  |
| [Create Doc](actions/p-ost-doc-id2e5679b3.md) | POST |  |

### Employee

| Action | Method | Description |
| --- | --- | --- |
| [Delete Employee](actions/d-elete-employee-id64ffa678.md) | DELETE |  |
| [Get Employee](actions/g-et-employee-id16d0319b.md) | GET |  |
| [List Employee](actions/list-employees.md) | GET |  |
| [Create Employee](actions/p-ost-employee-id714ff83f.md) | POST |  |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Delete Invoice](actions/d-elete-invoice-ide74e1ad6.md) | DELETE |  |
| [Get Invoice](actions/g-et-invoice-id8e70400e.md) | GET |  |
| [List Invoice](actions/g-et-invoice1d8b0201.md) | GET |  |
| [Create Invoice](actions/p-ost-invoice-id53d8209e.md) | POST |  |
| [Create Invoice](actions/p-ost-invoice842da1cb.md) | POST |  |

### Offer

| Action | Method | Description |
| --- | --- | --- |
| [Delete Offer](actions/d-elete-offer-id540925e9.md) | DELETE |  |
| [Get Offer](actions/g-et-offer-id39ddcb56.md) | GET |  |
| [List Offer](actions/g-et-offer10016cf4.md) | GET |  |
| [Create Offer](actions/p-ost-offer-idb50e0bb9.md) | POST |  |
| [Create Offer](actions/p-ost-offerd5088682.md) | POST |  |

### Payer

| Action | Method | Description |
| --- | --- | --- |
| [Get Payer](actions/g-et-payer-iddd531ac2.md) | GET |  |
| [List Payer](actions/g-et-payer5c29f374.md) | GET |  |
| [Create Payer](actions/p-ost-payer-id3411f266.md) | POST |  |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Delete Project](actions/d-elete-project-id8631b37c.md) | DELETE |  |
| [Get Project](actions/g-et-project-id73f4bff9.md) | GET |  |
| [List Project](actions/g-et-project0d814dd1.md) | GET |  |
| [Create Project](actions/p-ost-project-id1e6817f1.md) | POST |  |
| [Create Project](actions/p-ost-projectd3d8267d.md) | POST |  |

### Search

| Action | Method | Description |
| --- | --- | --- |
| [List Search](actions/g-et-doc-search3c62370c.md) | GET |  |
| [List Search](actions/g-et-employee-search359d76fa.md) | GET |  |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Delete Task](actions/d-elete-task-id775df228.md) | DELETE |  |
| [Get Task](actions/g-et-task-id018e080a.md) | GET |  |
| [List Task](actions/g-et-task756a2c73.md) | GET |  |
| [Create Task](actions/p-ost-task-id5a20d930.md) | POST |  |
| [Create Task](actions/p-ost-task601fca78.md) | POST |  |

### Todo

| Action | Method | Description |
| --- | --- | --- |
| [Delete Todo](actions/d-elete-todo-id2ad282d1.md) | DELETE |  |
| [Get Todo](actions/g-et-todo-id43c4df78.md) | GET |  |
| [List Todo](actions/g-et-todoaefb15e4.md) | GET |  |
| [Create Todo](actions/p-ost-todo-id9c49f41d.md) | POST |  |
| [Create Todo](actions/p-ost-todoec4f080e.md) | POST |  |

### Warehouse

| Action | Method | Description |
| --- | --- | --- |
| [Get Warehouse](actions/g-et-warehouse-id4c772427.md) | GET |  |
| [List Warehouse](actions/g-et-warehouse30b14284.md) | GET |  |
| [Create Warehouse](actions/p-ost-warehouse-id7a0bbd4c.md) | POST |  |

