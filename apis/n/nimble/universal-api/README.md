# <img src="https://images.mindcloud.co/apps/icons/nimble_1773958238822.png" alt="Nimble logo" width="28" height="28"> Nimble: Universal API

Manage Nimble contacts, leads, deals, pipelines, notes, and draft messages.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nimble/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.nimble.com/
- **Vendor API docs:** https://www.nimble.com/developers/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nimble/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Activities

| Action | Method | Description |
| --- | --- | --- |
| [List Contact Proceedings](actions/list-contact-proceedings.md) | GET | Retrieves proceedings for a contact from Nimble. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Assign Tags to Contact](actions/assign-tags-to-contact.md) | PUT | Updates tags for a contact in Nimble. |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Nimble. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Nimble. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Nimble by ID. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves a filtered list of contacts from Nimble. |
| [Search Contacts by Identifiers](actions/search-contacts-by-identifiers.md) | GET |  |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Nimble. |

### Deals

| Action | Method | Description |
| --- | --- | --- |
| [Create Deal](actions/create-deal.md) | POST | Creates a new deal in Nimble. |
| [Delete Deal](actions/delete-deal.md) | DELETE | Deletes an existing deal from Nimble. |
| [Get Deal](actions/get-deal.md) | GET | Retrieves a deal from Nimble by ID. |
| [List Deals](actions/list-deals.md) | GET | Retrieves a list of deals from Nimble. |
| [Update Deal](actions/update-deal.md) | PUT | Updates an existing deal in Nimble. |

### Leads

| Action | Method | Description |
| --- | --- | --- |
| [Exit Lead from Pipeline Successfully](actions/exit-lead-from-pipeline-successfully.md) | PUT | Marks a lead as successfully exited from a Nimble pipeline. |
| [Exit Lead from Pipeline Unsuccessfully](actions/exit-lead-from-pipeline-unsuccessfully.md) | PUT | Marks a lead as unsuccessfully exited from a Nimble pipeline. |
| [Move Lead To Pipeline Stage](actions/move-lead-to-pipeline-stage.md) | PUT | Moves a lead to a pipeline stage in Nimble. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Create Draft Message](actions/create-draft-message.md) | POST | Creates a draft message in Nimble. |

### Notes

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact Note](actions/create-contact-note.md) | POST | Creates a note for one or more Nimble contacts. |
| [Delete Contact Note](actions/delete-contact-note.md) | DELETE | Deletes an existing contact note from Nimble. |
| [List Contact Notes](actions/list-contact-notes.md) | GET | Retrieves notes for a contact from Nimble. |
| [Update Contact Note](actions/update-contact-note.md) | PUT | Updates an existing note for Nimble contacts. |

### Pipelines

| Action | Method | Description |
| --- | --- | --- |
| [List Contact Pipelines](actions/list-contact-pipelines.md) | GET | Retrieves available contact pipelines from Nimble. |
| [List Deal Pipelines](actions/list-deal-pipelines.md) | GET | Retrieves available deal pipelines from Nimble. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the authenticated user from Nimble. |

