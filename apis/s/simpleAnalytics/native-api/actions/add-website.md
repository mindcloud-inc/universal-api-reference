# Add Website with Simple Analytics

Creates a new website in Simple Analytics.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/websites/add`
- **Base URL:** `https://simpleanalytics.com`
- **Official documentation:** [Add Website](https://docs.simpleanalytics.com/api/admin)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hostname` | body | `string` | yes | Hostname to add, for example `example.com`. |
| `timezone` | body | `string` | no | IANA time zone for the new website. |
| `public` | body | `boolean` | no | Whether the website should be public. |
| `label` | body | `string` | no | Optional label shown on the websites overview page. |
