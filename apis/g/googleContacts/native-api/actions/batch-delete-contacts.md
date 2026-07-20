# Batch Delete Contacts with Google Contacts

Deletes multiple contacts from Google Contacts.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/people\:batchDeleteContacts`
- **Base URL:** `https://people.googleapis.com`
- **Official documentation:** [Batch Delete Contacts](https://developers.google.com/people/api/rest/v1/people/batchDeleteContacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resourceNames[]` | body | `array<string>` | yes | Array of contact resource names to delete (e.g. people/c123). |
