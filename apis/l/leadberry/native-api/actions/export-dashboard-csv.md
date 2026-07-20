# Export Dashboard CSV with Leadberry

## Endpoint

- **Method:** `POST`
- **Path:** `/data/downloadCSVFromDashboard`
- **Base URL:** `https://app.leadberry.com`
- **Official documentation:** [Export Dashboard CSV](https://app.leadberry.com/js/dist/all.min.js?ver=20221103_1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `allResults` | body | `string` | no | Dashboard results payload to export. |
| `companyAndSocialData` | body | `string` | no | Whether to include company and social data in the export. |
| `emailAddresses` | body | `string` | no | Whether to include email addresses in the export. |
| `extraData.aid` | body | `string` | no | Leadberry account ID for the exported dashboard view. |
| `extraData.exportFrom` | body | `string` | no | Export start date. |
| `extraData.exportTo` | body | `string` | no | Export end date. |
| `extraData.pid` | body | `string` | no | Leadberry profile ID for the exported dashboard view. |
| `extraData.profileName` | body | `string` | no | Profile name for the exported dashboard view. |
| `extraData.websiteUrl` | body | `string` | no | Website URL for the exported dashboard view. |
| `extraData.wid` | body | `string` | no | Leadberry website ID for the exported dashboard view. |
