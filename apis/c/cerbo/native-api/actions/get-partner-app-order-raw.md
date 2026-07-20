# Get Partner App Order Raw with Cerbo

Retrieves the raw Quest requisition document from Cerbo.

## Endpoint

- **Method:** `GET`
- **Path:** `/partners/quest/requisition/:order_id/content`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Get Partner App Order Raw](https://docs.cer.bo/#tag/Partner-Applications/operation/showPartnerAppOrderRaw)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_id` | path | `number` | no | ID of order to show |
