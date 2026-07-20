# Update Styleguide Text Style with Zeplin

Updates an existing styleguide text style in Zeplin.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/styleguides/{styleguide_id}/text_styles/{text_style_id}`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [Update Styleguide Text Style](https://docs.zeplin.dev/reference/updatestyleguidetextstyle)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `styleguide_id` | path | `string` | yes | Styleguide id |
| `text_style_id` | path | `string` | yes | Text style id |
| `name` | body | `string` | yes | Name of the text style |
| `color` | body | `object` | yes | — |
