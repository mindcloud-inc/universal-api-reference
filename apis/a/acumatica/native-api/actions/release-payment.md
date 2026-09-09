# Release Payment with Acumatica

## Endpoint

- **Method:** `POST`
- **Path:** `/entity/{endpointName}/{endpointVersion}/Payment/ReleasePayment`
- **Base URL:** `{uRL}`
- **Official documentation:** [Release Payment](https://help.acumatica.com/Wiki/ShowWiki.aspx?PageID=91dda8ed-5e92-48a5-a176-9a255506d0d6&wikiname=HelpRoot_Dev_Integration)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `entity` | body | `object` | no |
| `entity.Type` | body | `object` | no |
| `entity.Type.value` | body | `string` | yes |
| `entity.ReferenceNbr` | body | `object` | no |
| `entity.ReferenceNbr.value` | body | `string` | yes |
