# Get Form JS Embed Code with AbcSubmit

Retrieves JavaScript embed code for an AbcSubmit form.

## Endpoint

- **Method:** `GET`
- **Path:** `/embed/:form_id/:seo_form_name.js`
- **Base URL:** `https://www.abcsubmit.com`
- **Official documentation:** [Get Form JS Embed Code](https://www.abcsubmit.com/site/api-documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_id` | path | `string` | yes | The ID of the form to embed. |
| `seo_form_name` | path | `string` | yes | The SEO form slug used in the embed script URL. |
