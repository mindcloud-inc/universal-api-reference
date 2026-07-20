# Get Users with Heymarket SMS

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/users/get`
- **Base URL:** `https://api.heymarket.com`
- **Official documentation:** [Get Users](https://heymarket.docs.apiary.io/api-description-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phone[]` | body | `array<string>` | no | Phone numbers of users to search for within the team. |
| `email[]` | body | `array<string>` | no | Email addresses of users to search for within the team. |
