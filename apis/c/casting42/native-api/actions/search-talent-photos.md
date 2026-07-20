# Search Talent Photos with Casting42

Finds talent photos in Casting42 by talent tag.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/talents/photos/find`
- **Base URL:** `https://casting42.com`
- **Official documentation:** [Search Talent Photos](https://documenter.getpostman.com/view/24607394/2s9YR6buRP)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `talentTags[]` | body | `array<string>` | yes | Array of talent tags to search photos for. |
| `photo_size` | body | `string` | no | Requested photo size, such as large. |
