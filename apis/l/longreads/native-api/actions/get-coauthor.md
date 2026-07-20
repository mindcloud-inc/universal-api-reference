# Get Coauthor with Longreads

Retrieves a Longreads coauthor by nicename.

## Endpoint

- **Method:** `GET`
- **Path:** `/coauthors/v1/coauthors/{user_nicename}`
- **Base URL:** `https://longreads.com/wp-json`
- **Official documentation:** [Get Coauthor](https://longreads.com/wp-json/coauthors/v1/coauthors/adminnewspack)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_nicename` | path | `string` | yes | The coauthor nicename slug to retrieve. |
