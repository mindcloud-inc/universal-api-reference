# List Relation Infos with ThingsBoard

## Endpoint

- **Method:** `GET`
- **Path:** `/relations/info`
- **Base URL:** `{baseUrl}/api`
- **Official documentation:** [List Relation Infos](https://thingsboard.cloud/swagger-ui/index.html#/entity-relation-controller/findInfoByTo)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fromId` | query | `string` | yes | The source entity ID. |
| `fromType` | query | `string` | yes | The source entity type, for example DEVICE. |
