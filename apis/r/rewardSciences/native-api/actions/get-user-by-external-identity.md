# Get User By External Identity with Reward Sciences

## Endpoint

- **Method:** `GET`
- **Path:** `/idps/:idp/:identity/user`
- **Base URL:** `https://api.rewardsciences.com`
- **Official documentation:** [Get User By External Identity](https://developers.rewardsciences.com/api/docs#managing-users-using-external-identities-fetch-user-info-using-external-identity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `idp` | path | `string` | yes | Identity provider name. |
| `identity` | path | `string` | yes | Identity value within the provider. |
