# Track Activity with Reward Sciences

## Endpoint

- **Method:** `POST`
- **Path:** `/activities`
- **Base URL:** `https://api.rewardsciences.com`
- **Official documentation:** [Track Activity](https://developers.rewardsciences.com/api/docs#tracking-user-activities)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idp` | body | `string` | yes | Identity provider name. |
| `identity` | body | `string` | yes | Identity value within the provider. |
| `activity_type` | body | `string` | yes | Case-insensitive activity identifier. |
| `fields` | body | `object` | no | Optional custom metadata object. |
