# Verify Member Token with Memberstack

## Endpoint

- **Method:** `POST`
- **Path:** `/members/verify-token`
- **Base URL:** `https://admin.memberstack.com`
- **Official documentation:** [Verify Member Token](https://developers.memberstack.com/admin-rest-api/verification)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `token` | body | `string` | yes | Member JWT token to verify. |
