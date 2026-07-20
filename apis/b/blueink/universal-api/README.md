# <img src="https://images.mindcloud.co/apps/icons/blueink_1774629406395.png" alt="Blueink logo" width="28" height="28"> Blueink: Universal API

Send, sign, and manage eSignature bundles and templates

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/blueink/latest
- **Category:** Productivity / Legal & Contracts
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.blueink.com
- **Vendor API docs:** https://developer.blueink.com/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Bundles](actions/list-bundles.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blueink/latest/actions/list-bundles?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Bundle

| Action | Method | Description |
| --- | --- | --- |
| [Add Bundle Tags](actions/add-bundle-tags.md) | PUT | Adds tags to a Blueink bundle. |
| [Cancel Bundle](actions/cancel-bundle.md) | PUT | Cancels an existing bundle in Blueink. |
| [Create Bundle](actions/create-bundle.md) | POST | Creates a new bundle in Blueink. |
| [Create Bundle from Envelope Template](actions/create-bundle-from-envelope-template.md) | POST | Creates a Blueink bundle from an envelope template. |
| [List Bundles](actions/list-bundles.md) | GET | Retrieves bundles from your Blueink account. |
| [Remove Bundle Tags](actions/remove-bundle-tags.md) | PUT | Removes tags from a Blueink bundle. |
| [Retrieve Bundle](actions/retrieve-bundle.md) | GET | Retrieves an existing bundle from Blueink. |
| [Update Bundle](actions/update-bundle.md) | PUT | Updates an existing bundle in Blueink. |

### Bundle Data

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Bundle Data](actions/retrieve-bundle-data.md) | GET | Retrieves field data for a Blueink bundle. |

### Bundle Event

| Action | Method | Description |
| --- | --- | --- |
| [List Bundle Events](actions/list-bundle-events.md) | GET | Retrieves event history for a Blueink bundle. |

### Bundle File

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Bundle Files](actions/retrieve-bundle-files.md) | GET | Retrieves files for a Blueink bundle. |

### Envelope Template

| Action | Method | Description |
| --- | --- | --- |
| [List Envelope Templates](actions/list-envelope-templates.md) | GET | Retrieves available envelope templates from Blueink. |

### Packet

| Action | Method | Description |
| --- | --- | --- |
| [Create Embedded Signing URL](actions/create-embedded-signing-url.md) | POST | Creates an embedded signing URL for a Blueink packet. |
| [Retrieve Packet](actions/retrieve-packet.md) | GET | Retrieves an existing packet from Blueink. |
| [Send Reminder](actions/send-packet-reminder.md) | PUT | Sends a reminder for a Blueink packet. |
| [Update Packet](actions/update-packet.md) | PUT | Updates an existing packet in Blueink. |

### Packet Certificate

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Packet Certificate of Evidence](actions/retrieve-packet-certificate-of-evidence.md) | GET | Retrieves a packet certificate of evidence from Blueink. |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Create Person](actions/create-person.md) | POST | Creates a new person in Blueink. |
| [Delete Person](actions/delete-person.md) | DELETE | Deletes an existing person from Blueink. |
| [List Persons](actions/list-persons.md) | GET | Retrieves persons from your Blueink account. |
| [Retrieve Person](actions/retrieve-person.md) | GET | Retrieves an existing person from Blueink. |
| [Update Person](actions/update-person.md) | PUT | Updates an existing person in Blueink. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [List Document Templates](actions/list-document-templates.md) | GET | Retrieves available document templates from Blueink. |
| [Retrieve Document Template](actions/retrieve-document-template.md) | GET | Retrieves a document template from Blueink. |

