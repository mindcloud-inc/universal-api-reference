# Publish Weld with Anvil

Publishes an existing weld in Anvil.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://graphql.useanvil.com`
- **Official documentation:** [Publish Weld](https://www.useanvil.com/docs/api/graphql/reference/#mutation-publishWeld)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.eid` | body | `string` | yes | Provide EID for Publish Weld. |
| `variables.title` | body | `string` | yes | Provide Title for Publish Weld. |
| `variables.description` | body | `string` | no | Provide Description for Publish Weld. |
| `variables.migrateOpenWeldDatas` | body | `boolean` | no | Provide Migrate Open Weld Datas for Publish Weld. |
