# Add Tag with Kaiten

Creates a tag in Kaiten.

## Endpoint

- **Method:** `POST`
- **Path:** `/tags`
- **Base URL:** `https://{companyDomain}.kaiten.ru/api/latest`
- **Official documentation:** [Add Tag](https://developers.kaiten.ru/tags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The tag name. |
| `color` | body | `number` | no | The numeric Kaiten tag color. |
