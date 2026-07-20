# Publish Credential with Sertifier

Publishes an existing credential in Sertifier.

## Endpoint

- **Method:** `POST`
- **Path:** `/credential/publish`
- **Base URL:** `https://b2b.sertifier.com`
- **Official documentation:** [Publish Credential](https://sertifier.docs.apiary.io/reference/credential/publish-credential)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids[]` | body | `array<string>` | yes | Send multiple values as a array. |
