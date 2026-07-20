# Prepare Full Transaction Import with Sales Cookie

Prepares a transaction import batch in Sales Cookie.

## Endpoint

- **Method:** `POST`
- **Path:** `/Api/PrepareImport`
- **Base URL:** `https://salescookie.com/app`
- **Official documentation:** [Prepare Full Transaction Import](https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-use-the-full-transaction-import-rest-api)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/xml` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataSource` | body | `string` | yes | Data source name sent in the X-DataSource header. |
| `mappingsXml` | body | `string` | yes | XML mappings document describing CSV field mappings. |
