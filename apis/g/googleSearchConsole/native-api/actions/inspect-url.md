# Inspect URL with Google Search Console

## Endpoint

- **Method:** `POST`
- **Path:** `https://searchconsole.googleapis.com/v1/urlInspection/index:inspect`
- **Base URL:** `https://www.googleapis.com/webmasters/v3`
- **Official documentation:** [Inspect URL](https://developers.google.com/webmaster-tools/v1/urlInspection.index/inspect)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inspectionUrl` | body | `string` | yes | Fully-qualified URL to inspect. It must be under the property specified in Site URL. |
| `siteUrl` | body | `list<string>` | yes | The Search Console property URL that contains the inspected URL. |
| `languageCode` | body | `string` | no | Optional IETF BCP-47 language code for translated issue messages. Google defaults this to en-US. |
