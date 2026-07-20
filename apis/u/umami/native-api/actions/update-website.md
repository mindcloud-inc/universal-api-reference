# Update Website with Umami

## Endpoint

- **Method:** `POST`
- **Path:** `/websites/:websiteId`
- **Base URL:** `https://api.umami.is/v1`
- **Official documentation:** [Update Website](https://docs.umami.is/docs/api/websites)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `websiteId` | path | `string` | yes | The website ID. |
| `name` | body | `string` | yes | The website name in Umami. |
| `domain` | body | `string` | yes | The full tracked domain. |
| `shareId` | body | `string` | no | A share URL identifier. Set null to unshare. |
