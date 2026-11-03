# List Orders with Rithum for Brands

## Endpoint

- **Method:** `GET`
- **Path:** `Orders`
- **Base URL:** `https://api.channeladvisor.com/v1/`
- **Official documentation:** [List Orders](https://knowledge.channeladvisor.com/kc?id=kb_article_view&sys_id=f00d5fc52fd15994cffb5ff62799b68f)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ProfileID` | query | `list<number>` | no | — |
| `siteName` | query | `string` | no | — |
| `dateModifiedAfter` | query | `date` | no | — |
| `dateModifiedBefore` | query | `date` | no | — |
| `$filter` | query | `string` | no | Examples: ProfileID eq ProfileID PaymentStatus eq 'Cleared' CreatedDateUtc ge 2016-03-02 and CreatedDateUtc lt 2016-03-03 BuyerEmailAddress eq 'first.last@example.com' |
| `$expand` | query | `string` | no | Examples: Items,Fulfillments Fulfillments($expand=Items) Items($expand=Adjustments),Fulfillments($expand=Items) (see https://knowledge.channeladvisor.com/kc?id=kb_article_view&sys_id=3fccd3491bd5d1d42d9eea40604bcb70) |
| `$select` | query | `string` | no | Return only selected fields |
| `exported` | query | `boolean` | no | — |
| `$orderby` | query | `string` | no | orderBy |
