# Get WhatsApp Group Contacts with WhatsBoost

Retrieves WhatsApp group contacts from WhatsBoost.

## Endpoint

- **Method:** `POST`
- **Path:** `/get/wa.group.contacts`
- **Base URL:** `https://whatsboost.net/api`
- **Official documentation:** [Get WhatsApp Group Contacts](https://whatsboost.net/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `unique` | body | `string` | yes | WhatsApp Unique ID |
| `gid` | body | `string` | yes | WhatsApp Group ID |
