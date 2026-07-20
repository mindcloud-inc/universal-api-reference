# Import Website with Filestage

Creates a website file in Filestage from a URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/files/import-website`
- **Base URL:** `https://api.filestage.io/ext/v2`
- **Official documentation:** [Import Website](https://developers.filestage.io/docs/api/0gstxpcjbyadr-import-website)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | body | `string` | yes | — |
| `stepIds[]` | body | `array<string>` | no | — |
| `url` | body | `string` | yes | — |
| `fileId` | body | `string` | no | — |
| `websiteMode` | body | `string` | no | proxy - imports the full website in the new mode. iframe - loads the website in the legacy viewer. |
| `callbackURL` | body | `string` | no | — |
| `callbackHeaders` | body | `object` | no | — |
