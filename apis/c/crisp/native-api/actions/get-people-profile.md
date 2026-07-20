# Get People Profile with Crisp

Retrieves a people profile from Crisp.

## Endpoint

- **Method:** `GET`
- **Path:** `/website/:website_id/people/profile/:people_id`
- **Base URL:** `https://api.crisp.chat/v1`
- **Official documentation:** [Get People Profile](https://docs.crisp.chat/references/rest-api/v1/#get-people-profile)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `website_id` | path | `string` | yes | The website identifier |
| `people_id` | path | `string` | yes | The people identifier or email |
