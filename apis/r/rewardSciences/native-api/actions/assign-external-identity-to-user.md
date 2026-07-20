# Assign External Identity To User with Reward Sciences

## Endpoint

- **Method:** `POST`
- **Path:** `/users/:userId/identities`
- **Base URL:** `https://api.rewardsciences.com`
- **Official documentation:** [Assign External Identity To User](https://developers.rewardsciences.com/api/docs#assigning-external-identities-to-a-user-assign-a-new-external-identity-to-a-user)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `number` | yes | The Reward Sciences user ID. |
| `idp` | body | `string` | yes | Identity provider name. |
| `identity` | body | `string` | yes | Identity value within the provider. |
