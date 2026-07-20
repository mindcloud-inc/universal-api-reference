# <img src="https://images.mindcloud.co/apps/icons/remberg-icon_1775854497529.png" alt="remberg logo" width="28" height="28"> remberg: Universal API

remberg API integration for assets, work orders, tickets, contacts, organizations, parts, forms, files, AI, and work requests.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/remberg/latest
- **Actions:** 45
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://remberg.de
- **Vendor API docs:** https://developers.remberg.de/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Assets](actions/list-assets.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/remberg/latest/actions/list-assets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (45)

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Delete Asset By Id](actions/delete-asset-by-id.md) | DELETE | Deletes an asset from remberg by internal ID. |
| [Delete Asset By Number](actions/delete-asset-by-number.md) | DELETE | Deletes an asset from remberg by asset number. |
| [Get Asset By Id](actions/get-asset-by-id.md) | GET | Retrieves an asset from remberg by internal ID. |
| [Get Asset By Number](actions/get-asset-by-number.md) | GET | Retrieves an asset from remberg by asset number. |
| [List Assets](actions/list-assets.md) | GET | Retrieves assets from remberg. |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [Get Ticket Categories](actions/get-ticket-categories.md) | GET | Retrieves ticket categories from remberg. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Delete Contact By Id](actions/delete-contact-by-id.md) | DELETE | Deletes a contact from remberg by ID. |
| [Get Contact By Id](actions/get-contact-by-id.md) | GET | Retrieves a contact from remberg by ID. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from remberg. |
| [List Organization Contacts](actions/list-organization-contacts.md) | GET | Retrieves contacts for an organization from remberg. |

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [Get Ticket Conversations](actions/get-ticket-conversations.md) | GET | Retrieves conversations for a remberg ticket. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Download File](actions/download-file.md) | GET | Downloads a file from remberg by ID. |
| [Get File By Id](actions/get-file-by-id.md) | GET | Retrieves file metadata from remberg by ID. |
| [List Files](actions/list-files.md) | GET | Retrieves files and folders from remberg. |
| [Resolve File Path](actions/resolve-file-path.md) | GET | Resolves a file or folder path in remberg. |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [Get Form By Id](actions/get-form-by-id.md) | GET | Retrieves a form from remberg by ID. |
| [List Forms](actions/list-forms.md) | GET | Retrieves forms from remberg. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [Delete Organization By Id](actions/delete-organization-by-id.md) | DELETE | Deletes an organization from remberg by ID. |
| [Get Organization By Id](actions/get-organization-by-id.md) | GET | Retrieves an organization from remberg by ID. |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organizations from remberg. |

### Service Requests

| Action | Method | Description |
| --- | --- | --- |
| [Approve Work Request By External Reference](actions/approve-work-request-by-external-reference.md) | PUT | Approves a work request in remberg by external reference. |
| [Approve Work Request By Id](actions/approve-work-request-by-id.md) | PUT | Approves a work request in remberg by internal ID. |
| [Decline Work Request By External Reference](actions/decline-work-request-by-external-reference.md) | PUT | Declines a work request in remberg by external reference. |
| [Decline Work Request By Id](actions/decline-work-request-by-id.md) | PUT | Declines a work request in remberg by internal ID. |
| [Delete Work Request By External Reference](actions/delete-work-request-by-external-reference.md) | DELETE | Deletes a work request from remberg by external reference. |
| [Delete Work Request By Id](actions/delete-work-request-by-id.md) | DELETE | Deletes a work request from remberg by internal ID. |
| [Get Work Request By External Reference](actions/get-work-request-by-external-reference.md) | GET | Retrieves a work request from remberg by external reference. |
| [Get Work Request By Id](actions/get-work-request-by-id.md) | GET | Retrieves a work request from remberg by internal ID. |
| [List Work Requests](actions/list-work-requests.md) | GET | Retrieves work requests from remberg. |

### Stock Movements

| Action | Method | Description |
| --- | --- | --- |
| [Get Work Order Stock Changes By External Reference](actions/get-work-order-stock-changes-by-external-reference.md) | GET | Retrieves stock changes for a remberg work order by external reference. |
| [Get Work Order Stock Changes By Id](actions/get-work-order-stock-changes-by-id.md) | GET | Retrieves stock changes for a remberg work order by ID. |

### Tickets

| Action | Method | Description |
| --- | --- | --- |
| [Delete Ticket By Id](actions/delete-ticket-by-id.md) | DELETE | Deletes a ticket from remberg by internal ID. |
| [Get Ticket By Id](actions/get-ticket-by-id.md) | GET | Retrieves a ticket from remberg by internal ID. |
| [List Tickets](actions/list-tickets.md) | GET | Retrieves tickets from remberg. |

### Timesheet Entries

| Action | Method | Description |
| --- | --- | --- |
| [Get Work Order Time Entries](actions/get-work-order-time-entries.md) | GET | Retrieves time entries for a remberg work order. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Delete Asset Type By Id](actions/delete-asset-type-by-id.md) | DELETE | Deletes an asset type from remberg by internal ID. |
| [Delete Asset Type By Label](actions/delete-asset-type-by-label.md) | DELETE | Deletes an asset type from remberg by label. |
| [Get Asset Type By Id](actions/get-asset-type-by-id.md) | GET | Retrieves an asset type from remberg by internal ID. |
| [Get Asset Type By Label](actions/get-asset-type-by-label.md) | GET | Retrieves an asset type from remberg by label. |
| [Get Failure Types](actions/get-failure-types.md) | GET | Retrieves failure types from remberg. |

### Work Orders

| Action | Method | Description |
| --- | --- | --- |
| [Delete Work Order By External Reference](actions/delete-work-order-by-external-reference.md) | DELETE | Deletes a work order from remberg by external reference. |
| [Delete Work Order By Id](actions/delete-work-order-by-id.md) | DELETE | Deletes a work order from remberg by internal ID. |
| [Get Work Order By External Reference](actions/get-work-order-by-external-reference.md) | GET | Retrieves a work order from remberg by external reference. |
| [Get Work Order By Id](actions/get-work-order-by-id.md) | GET | Retrieves a work order from remberg by internal ID. |
| [List Work Orders](actions/list-work-orders.md) | GET | Retrieves work orders from remberg. |

