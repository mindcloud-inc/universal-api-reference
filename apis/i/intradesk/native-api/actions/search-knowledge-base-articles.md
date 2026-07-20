# Search Knowledge Base Articles with Intradesk

Finds knowledge base articles in Intradesk by search text.

## Endpoint

- **Method:** `GET`
- **Path:** `/knowledgebase/api/v1/Hints/search`
- **Base URL:** `https://apigw.intradesk.ru`
- **Official documentation:** [Search Knowledge Base Articles](https://apigw.intradesk.ru/knowledgebase_docs/swagger/index.html#/Hints/get_api_v1_Hints_search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `searchString` | query | `string` | no | Knowledge base hint search text. |
| `skip` | query | `number` | no | Number of knowledge base hint results to skip. Defaults to 0. |
| `take` | query | `number` | no | Maximum number of knowledge base hint results to return. Defaults to 10. |
| `servicePath` | query | `string` | no | Optional service path filter for knowledge base hints. |
