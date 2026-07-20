# Get People Data with Crisp

Retrieves people data from Crisp.

## Endpoint

- **Method:** `GET`
- **Path:** `/website/:website_id/people/data/:people_id`
- **Base URL:** `https://api.crisp.chat/v1`
- **Official documentation:** [Get People Data](https://docs.crisp.chat/references/rest-api/v1/#get-people-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `website_id` | path | `string` | yes | The website identifier. |
| `people_id` | path | `string` | yes | The people identifier or people email. |
