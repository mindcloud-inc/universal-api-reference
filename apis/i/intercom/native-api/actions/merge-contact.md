# Merge Contact with Intercom

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/merge`
- **Base URL:** `https://api.intercom.io`
- **Official documentation:** [Merge Contact](https://developers.intercom.com/docs/references/rest-api/api.intercom.io/contacts/mergecontact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | yes | Intercom lead contact ID to merge from |
| `into` | body | `string` | yes | Intercom user contact ID to merge into |
