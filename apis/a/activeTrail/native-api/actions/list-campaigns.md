# List Campaigns with ActiveTrail

Retrieves a list of campaigns from ActiveTrail.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns`
- **Base URL:** `https://webapi.mymarketing.co.il/api`
- **Official documentation:** [List Campaigns](https://webapi.mymarketing.co.il/api/docs/and/Api/GET-api-campaigns_MailingListId_ContentCategoryId_SearchTerm_SendType_FromDate_ToDate_Page_Limit)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ContentCategoryId` | query | `number` | no | Limit campaigns to a content category. |
| `FromDate` | query | `date` | no | Only include campaigns from this date forward. |
| `MailingListId` | query | `number` | no | Limit campaigns to a mailing list. |
| `SearchTerm` | query | `string` | no | Search campaigns by a free-text term. |
| `SendType` | query | `string` | no | Limit campaigns to a send type. |
| `ToDate` | query | `date` | no | Only include campaigns up to this date. |
