# Create Audience Member with HeyPoplar

Creates an audience member in HeyPoplar.

## Endpoint

- **Method:** `POST`
- **Path:** `/audience/:id`
- **Base URL:** `https://api.heypoplar.com/v1`
- **Official documentation:** [Create Audience Member](https://docs.heypoplar.com/api/endpoints/audience#create-audience-member)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID of the audience to add the member to. |
| `email` | body | `string` | yes | Email address for the audience member. |
