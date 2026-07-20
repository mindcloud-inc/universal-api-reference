# Check Disposable Domain with EmailListVerify

Checks whether a domain is disposable in EmailListVerify.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/checkDisposable`
- **Base URL:** `https://api.emaillistverify.com`
- **Official documentation:** [Check Disposable Domain](https://api.emaillistverify.com/api-doc#/Verification%20Endpoints/checkDisposable)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | query | `string` | yes | Email domain to check for disposable-address behavior. |
