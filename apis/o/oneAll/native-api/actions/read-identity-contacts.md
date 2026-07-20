# Read Identity Contacts with OneAll

Retrieves an identity's social contacts from OneAll.

## Endpoint

- **Method:** `GET`
- **Path:** `/identities/<identity_token>/contacts.json`
- **Base URL:** `https://mindcloudco.api.oneall.com`
- **Official documentation:** [Read Identity Contacts](https://docs.oneall.com/api/resources/identities/read-contacts/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identity_token` | path | `string` | yes | The OneAll identity token. |
