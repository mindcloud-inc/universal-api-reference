# Get Temporary Public File URLs with Fibery

Retrieves temporary public file URLs from Fibery.

## Endpoint

- **Method:** `POST`
- **Path:** `/files/sign-urls`
- **Base URL:** `https://{account}.fibery.io/api`
- **Official documentation:** [Get Temporary Public File URLs](https://the.fibery.io/@public/User_Guide/Guide/File-API-265)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `secrets[]` | body | `array<string>` | yes | Array of file secrets to sign. |
