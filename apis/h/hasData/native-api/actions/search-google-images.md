# Search Google Images with HasData

Retrieves Google Images results from HasData.

## Endpoint

- **Method:** `GET`
- **Path:** `/scrape/google/images`
- **Base URL:** `https://api.hasdata.com`
- **Official documentation:** [Search Google Images](https://docs.hasdata.com/apis/google-images/images)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `deviceType` | query | `string` | no | Device type for the image search, such as desktop. |
| `ijn` | query | `number` | no | Image result page number, where 0 is the first page. |
| `location` | query | `string` | no | Google canonical location for the image search. |
| `q` | query | `string` | yes | Search query for Google Images. |
