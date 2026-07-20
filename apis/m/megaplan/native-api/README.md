# Megaplan: Native API Reference

A consolidated summary of Megaplan's API configuration and 60 documented operations, with links to official documentation.

- **Official docs:** https://m60888876.megaplan.ru/api/v3/docs
- **OpenAPI specification:** https://m60888876.megaplan.ru/api/v3
- **API base URL:** `https://m60888876.megaplan.ru/api/v3`

## Authentication

### Megaplan access token

Stores a Megaplan API v3 bearer access token generated from the tenant token endpoint.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://m60888876.megaplan.ru/api/v3/docs)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (60 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete Contractor Company](actions/d-elete-contractor-company-idf1fb1f9b.md) | `DELETE /contractorCompany/:id` | [docs](https://m60888876.megaplan.ru/api/v3/docs#contractorCompanyid) |
| [Delete Contractor Human](actions/d-elete-contractor-human-idc1874191.md) | `DELETE /contractorHuman/:id` | [docs](https://m60888876.megaplan.ru/api/v3/docs#contractorHumanid) |
| [Delete Deal](actions/d-elete-deal-id25a61849.md) | `DELETE /deal/:id` | [docs](https://m60888876.megaplan.ru/api/v3/docs#dealid) |
| [Delete Doc](actions/d-elete-doc-ideef30a90.md) | `DELETE /doc/:id` | [docs](https://m60888876.megaplan.ru/api/v3/docs#docid) |
| [Delete Employee](actions/d-elete-employee-id64ffa678.md) | `DELETE /employee/:id` | [docs](https://m60888876.megaplan.ru/api/v3/docs#employeeid) |
| [Delete Invoice](actions/d-elete-invoice-ide74e1ad6.md) | `DELETE /invoice/:id` | [docs](https://m60888876.megaplan.ru/api/v3/docs#invoiceid) |
| [Delete Offer](actions/d-elete-offer-id540925e9.md) | `DELETE /offer/:id` | [docs](https://m60888876.megaplan.ru/api/v3/docs#offerid) |
| [Delete Project](actions/d-elete-project-id8631b37c.md) | `DELETE /project/:id` | [docs](https://m60888876.megaplan.ru/api/v3/docs#projectid) |
| [Delete Task](actions/d-elete-task-id775df228.md) | `DELETE /task/:id` | [docs](https://m60888876.megaplan.ru/api/v3/docs#taskid) |
| [Delete Todo](actions/d-elete-todo-id2ad282d1.md) | `DELETE /todo/:id` | [docs](https://m60888876.megaplan.ru/api/v3/docs#todoid) |
| [Get Consignment](actions/g-et-consignment-id89c79c96.md) | `GET /consignment/:id` | [docs](https://m60888876.megaplan.ru/api/v3/docs#consignmentid) |
| [List Consignment](actions/g-et-consignment8475e2fc.md) | `GET /consignment` | [docs](https://m60888876.megaplan.ru/api/v3/docs#consignment) |
| [Get Contractor Company](actions/g-et-contractor-company-idd2a96eab.md) | `GET /contractorCompany/:id` | [docs](https://m60888876.megaplan.ru/api/v3/docs#contractorCompanyid) |
| [List Contractor Company](actions/g-et-contractor-company9e68924f.md) | `GET /contractorCompany` | [docs](https://m60888876.megaplan.ru/api/v3/docs#contractorCompany) |
| [Get Contractor Human](actions/g-et-contractor-human-id161a9507.md) | `GET /contractorHuman/:id` | [docs](https://m60888876.megaplan.ru/api/v3/docs#contractorHumanid) |
| [List Contractor Human](actions/g-et-contractor-human1cb34131.md) | `GET /contractorHuman` | [docs](https://m60888876.megaplan.ru/api/v3/docs#contractorHuman) |
| [Get Deal](actions/g-et-deal-ida67919a2.md) | `GET /deal/:id` | [docs](https://m60888876.megaplan.ru/api/v3/docs#dealid) |
| [List Deal](actions/g-et-deal502406fe.md) | `GET /deal` | [docs](https://m60888876.megaplan.ru/api/v3/docs#deal) |
| [Get Doc](actions/g-et-doc-id824f6a06.md) | `GET /doc/:id` | [docs](https://m60888876.megaplan.ru/api/v3/docs#docid) |
| [List Search](actions/g-et-doc-search3c62370c.md) | `GET /doc/search` | [docs](https://m60888876.megaplan.ru/api/v3/docs#docsearch) |
| [List Doc](actions/g-et-doc34f3e930.md) | `GET /doc` | [docs](https://m60888876.megaplan.ru/api/v3/docs#doc) |
| [Get Employee](actions/g-et-employee-id16d0319b.md) | `GET /employee/:id` | [docs](https://m60888876.megaplan.ru/api/v3/docs#employeeid) |
| [List Search](actions/g-et-employee-search359d76fa.md) | `GET /employee/search` | [docs](https://m60888876.megaplan.ru/api/v3/docs#employeesearch) |
| [Get Invoice](actions/g-et-invoice-id8e70400e.md) | `GET /invoice/:id` | [docs](https://m60888876.megaplan.ru/api/v3/docs#invoiceid) |
| [List Invoice](actions/g-et-invoice1d8b0201.md) | `GET /invoice` | [docs](https://m60888876.megaplan.ru/api/v3/docs#invoice) |
| [Get Offer](actions/g-et-offer-id39ddcb56.md) | `GET /offer/:id` | [docs](https://m60888876.megaplan.ru/api/v3/docs#offerid) |
| [List Offer](actions/g-et-offer10016cf4.md) | `GET /offer` | [docs](https://m60888876.megaplan.ru/api/v3/docs#offer) |
| [Get Payer](actions/g-et-payer-iddd531ac2.md) | `GET /payer/:id` | [docs](https://m60888876.megaplan.ru/api/v3/docs#payerid) |
| [List Payer](actions/g-et-payer5c29f374.md) | `GET /payer` | [docs](https://m60888876.megaplan.ru/api/v3/docs#payer) |
| [Get Project](actions/g-et-project-id73f4bff9.md) | `GET /project/:id` | [docs](https://m60888876.megaplan.ru/api/v3/docs#projectid) |
| [List Project](actions/g-et-project0d814dd1.md) | `GET /project` | [docs](https://m60888876.megaplan.ru/api/v3/docs#project) |
| [Get Task](actions/g-et-task-id018e080a.md) | `GET /task/:id` | [docs](https://m60888876.megaplan.ru/api/v3/docs#taskid) |
| [List Task](actions/g-et-task756a2c73.md) | `GET /task` | [docs](https://m60888876.megaplan.ru/api/v3/docs#task) |
| [Get Todo](actions/g-et-todo-id43c4df78.md) | `GET /todo/:id` | [docs](https://m60888876.megaplan.ru/api/v3/docs#todoid) |
| [List Todo](actions/g-et-todoaefb15e4.md) | `GET /todo` | [docs](https://m60888876.megaplan.ru/api/v3/docs#todo) |
| [Get Warehouse](actions/g-et-warehouse-id4c772427.md) | `GET /warehouse/:id` | [docs](https://m60888876.megaplan.ru/api/v3/docs#warehouseid) |
| [List Warehouse](actions/g-et-warehouse30b14284.md) | `GET /warehouse` | [docs](https://m60888876.megaplan.ru/api/v3/docs#warehouse) |
| [List Account Info](actions/get-account-info.md) | `GET /accountInfo` | [docs](https://m60888876.megaplan.ru/api/v3/docs#accountInfo) |
| [List Employee](actions/list-employees.md) | `GET /employee` | [docs](https://m60888876.megaplan.ru/api/v3/docs#employee) |
| [Create Consignment](actions/p-ost-consignment-ide28969a6.md) | `POST /consignment/:id` | [docs](https://m60888876.megaplan.ru/api/v3/docs#consignmentid) |
| [Create Contractor Company](actions/p-ost-contractor-company-idf0ed4ae2.md) | `POST /contractorCompany/:id` | [docs](https://m60888876.megaplan.ru/api/v3/docs#contractorCompanyid) |
| [Create Contractor Company](actions/p-ost-contractor-company6a39dd15.md) | `POST /contractorCompany` | [docs](https://m60888876.megaplan.ru/api/v3/docs#contractorCompany) |
| [Create Contractor Human](actions/p-ost-contractor-human-id6294d755.md) | `POST /contractorHuman/:id` | [docs](https://m60888876.megaplan.ru/api/v3/docs#contractorHumanid) |
| [Create Contractor Human](actions/p-ost-contractor-human44f33981.md) | `POST /contractorHuman` | [docs](https://m60888876.megaplan.ru/api/v3/docs#contractorHuman) |
| [Create Deal](actions/p-ost-deal-id44864281.md) | `POST /deal/:id` | [docs](https://m60888876.megaplan.ru/api/v3/docs#dealid) |
| [Create Deal](actions/p-ost-dealff9859b3.md) | `POST /deal` | [docs](https://m60888876.megaplan.ru/api/v3/docs#deal) |
| [Create Doc](actions/p-ost-doc-id2e5679b3.md) | `POST /doc/:id` | [docs](https://m60888876.megaplan.ru/api/v3/docs#docid) |
| [Create Employee](actions/p-ost-employee-id714ff83f.md) | `POST /employee/:id` | [docs](https://m60888876.megaplan.ru/api/v3/docs#employeeid) |
| [Create Invoice](actions/p-ost-invoice-id53d8209e.md) | `POST /invoice/:id` | [docs](https://m60888876.megaplan.ru/api/v3/docs#invoiceid) |
| [Create Invoice](actions/p-ost-invoice842da1cb.md) | `POST /invoice` | [docs](https://m60888876.megaplan.ru/api/v3/docs#invoice) |
| [Create Offer](actions/p-ost-offer-idb50e0bb9.md) | `POST /offer/:id` | [docs](https://m60888876.megaplan.ru/api/v3/docs#offerid) |
| [Create Offer](actions/p-ost-offerd5088682.md) | `POST /offer` | [docs](https://m60888876.megaplan.ru/api/v3/docs#offer) |
| [Create Payer](actions/p-ost-payer-id3411f266.md) | `POST /payer/:id` | [docs](https://m60888876.megaplan.ru/api/v3/docs#payerid) |
| [Create Project](actions/p-ost-project-id1e6817f1.md) | `POST /project/:id` | [docs](https://m60888876.megaplan.ru/api/v3/docs#projectid) |
| [Create Project](actions/p-ost-projectd3d8267d.md) | `POST /project` | [docs](https://m60888876.megaplan.ru/api/v3/docs#project) |
| [Create Task](actions/p-ost-task-id5a20d930.md) | `POST /task/:id` | [docs](https://m60888876.megaplan.ru/api/v3/docs#taskid) |
| [Create Task](actions/p-ost-task601fca78.md) | `POST /task` | [docs](https://m60888876.megaplan.ru/api/v3/docs#task) |
| [Create Todo](actions/p-ost-todo-id9c49f41d.md) | `POST /todo/:id` | [docs](https://m60888876.megaplan.ru/api/v3/docs#todoid) |
| [Create Todo](actions/p-ost-todoec4f080e.md) | `POST /todo` | [docs](https://m60888876.megaplan.ru/api/v3/docs#todo) |
| [Create Warehouse](actions/p-ost-warehouse-id7a0bbd4c.md) | `POST /warehouse/:id` | [docs](https://m60888876.megaplan.ru/api/v3/docs#warehouseid) |
