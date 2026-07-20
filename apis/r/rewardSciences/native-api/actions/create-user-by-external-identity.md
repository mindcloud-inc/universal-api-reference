# Create User By External Identity with Reward Sciences

## Endpoint

- **Method:** `POST`
- **Path:** `/idps/:idp/:identity/user`
- **Base URL:** `https://api.rewardsciences.com`
- **Official documentation:** [Create User By External Identity](https://developers.rewardsciences.com/api/docs#managing-users-using-external-identities-create-a-user-using-an-external-identity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idp` | path | `string` | yes | Identity provider name. |
| `identity` | path | `string` | yes | Identity value within the provider. |
