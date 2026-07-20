# Publish HTML with Upload to URL

## Endpoint

- **Method:** `POST`
- **Path:** `/api/publish`
- **Base URL:** `https://uploadtourl.com`
- **Official documentation:** [Publish HTML](https://uploadtourl.com/api-docs)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `html_code` | body | `string` | yes | Raw HTML code to publish. |
| `page_path` | body | `string` | yes | Public path for the published page (for example: my-landing-page). |
| `subdomain` | body | `string` | no | Optional subdomain name. |
| `expiry_days` | body | `string` | no | Optional number of days before the published page expires. |
