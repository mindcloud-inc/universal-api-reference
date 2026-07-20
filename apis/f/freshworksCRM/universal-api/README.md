# <img src="https://images.mindcloud.co/apps/icons/freshworks-crm_1771969888167.png" alt="Freshworks CRM logo" width="28" height="28"> Freshworks CRM: Universal API

Manage contacts, accounts, deals, tasks, and CRM searches

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/freshworksCRM/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 107
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.freshworks.com/crm/suite/
- **Vendor API docs:** https://developers.freshworks.com/crm/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contact Fields](actions/list-contact-fields.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/list-contact-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (107)

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Delete Accounts](actions/bulk-delete-accounts.md) | DELETE | Deletes multiple sales accounts from Freshworks CRM. |
| [Bulk Upsert Accounts](actions/bulk-upsert-accounts.md) | PUT | Finds or creates multiple sales accounts in Freshworks CRM. |
| [Clone Account](actions/clone-account.md) | POST | Creates a sales account by cloning one in Freshworks CRM. |
| [Create Sales Account](actions/create-sales-account.md) | POST | Creates a new sales account in Freshworks CRM. |
| [Delete Sales Account](actions/delete-sales-account.md) | DELETE | Deletes an existing sales account from Freshworks CRM. |
| [Forget Account](actions/forget-account.md) | DELETE | Permanently deletes a sales account from Freshworks CRM. |
| [Get Sales Account](actions/get-sales-account.md) | GET | Retrieves a sales account from Freshworks CRM. |
| [List Sales Account Fields](actions/list-sales-account-fields.md) | GET | Retrieves sales account fields from Freshworks CRM. |
| [List Sales Accounts](actions/list-sales-accounts.md) | GET | Retrieves sales accounts from a view in Freshworks CRM. |
| [Update Account Team](actions/update-account-team.md) | PUT | Updates team members for a sales account in Freshworks CRM. |
| [Update Sales Account](actions/update-sales-account.md) | PUT | Updates an existing sales account in Freshworks CRM. |
| [Upsert Account](actions/upsert-account.md) | PUT | Finds a sales account in Freshworks CRM, or creates one when none match. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Add Contacts To List](actions/add-contacts-to-list.md) | PUT | Adds contacts to a list in Freshworks CRM. |
| [Bulk Assign Contact Owner](actions/bulk-assign-contact-owner.md) | PUT | Updates contact owners in Freshworks CRM in bulk. |
| [Bulk Delete Contacts](actions/bulk-delete-contacts.md) | DELETE | Deletes multiple contacts from Freshworks CRM. |
| [Bulk Delete Custom Module Records](actions/bulk-delete-custom-module-records.md) | DELETE | Deletes multiple custom module records from Freshworks CRM. |
| [Bulk Upsert Contacts](actions/bulk-upsert-contacts.md) | PUT | Finds or creates multiple contacts in Freshworks CRM. |
| [Clone Contact](actions/clone-contact.md) | POST | Creates a contact by cloning one in Freshworks CRM. |
| [Clone Custom Module Record](actions/clone-custom-module-record.md) | POST | Creates a custom module record by cloning one in Freshworks CRM. |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Freshworks CRM. |
| [Create Custom Module](actions/create-custom-module.md) | POST | Creates a custom module in Freshworks CRM. |
| [Create Custom Module Field](actions/create-custom-module-field.md) | POST | Creates a custom module field in Freshworks CRM. |
| [Create Custom Module Record](actions/create-custom-module-record.md) | POST | Creates a custom module record in Freshworks CRM. |
| [Create List](actions/create-list.md) | POST | Creates a new list in Freshworks CRM. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Freshworks CRM. |
| [Delete Custom Module](actions/delete-custom-module.md) | DELETE | Deletes a custom module from Freshworks CRM. |
| [Delete Custom Module Record](actions/delete-custom-module-record.md) | DELETE | Deletes a custom module record from Freshworks CRM. |
| [Forget Contact](actions/forget-contact.md) | DELETE | Permanently deletes a contact from Freshworks CRM. |
| [Forget Custom Module Record](actions/forget-custom-module-record.md) | DELETE | Permanently deletes a custom module record from Freshworks CRM. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Freshworks CRM. |
| [Get Custom Module](actions/get-custom-module.md) | GET | Retrieves a custom module from Freshworks CRM. |
| [Get Custom Module Record](actions/get-custom-module-record.md) | GET | Retrieves a custom module record from Freshworks CRM. |
| [List Contact Activities](actions/list-contact-activities.md) | GET | Retrieves activities for a contact in Freshworks CRM. |
| [List Contact Fields](actions/list-contact-fields.md) | GET | Retrieves contact fields from Freshworks CRM. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from a view in Freshworks CRM. |
| [List Contacts In List](actions/list-contacts-in-list.md) | GET | Retrieves contacts from a list in Freshworks CRM. |
| [List Custom Module Fields](actions/list-custom-module-fields.md) | GET | Retrieves custom module fields from Freshworks CRM. |
| [List Lists](actions/list-lists.md) | GET | Retrieves all lists from Freshworks CRM. |
| [Lookup Search](actions/lookup-search.md) | GET | Finds matching lookup records in Freshworks CRM. |
| [Move Contacts Between Lists](actions/move-contacts-between-lists.md) | PUT | Moves contacts between lists in Freshworks CRM. |
| [Remove Contacts From List](actions/remove-contacts-from-list.md) | PUT | Removes contacts from a list in Freshworks CRM. |
| [Search Records](actions/search-records.md) | GET | Finds matching records in Freshworks CRM. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Freshworks CRM. |
| [Update Contact Team](actions/update-contact-team.md) | PUT | Updates team members for a contact in Freshworks CRM. |
| [Update Custom Module](actions/update-custom-module.md) | PUT | Updates a custom module in Freshworks CRM. |
| [Update Custom Module Record](actions/update-custom-module-record.md) | PUT | Updates a custom module record in Freshworks CRM. |
| [Update List](actions/update-list.md) | PUT | Updates an existing list in Freshworks CRM. |
| [Upsert Contact](actions/upsert-contact.md) | PUT | Finds a contact in Freshworks CRM, or creates one if no match is found. |

### Deals

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Assign Document Owner](actions/bulk-assign-document-owner.md) | PUT | Updates document owners in Freshworks CRM in bulk. |
| [Bulk Delete Deals](actions/bulk-delete-deals.md) | DELETE | Deletes multiple deals from Freshworks CRM. |
| [Bulk Delete Documents](actions/bulk-delete-documents.md) | DELETE | Deletes multiple documents from Freshworks CRM. |
| [Bulk Restore Documents](actions/bulk-restore-documents.md) | PUT | Restores multiple documents in Freshworks CRM. |
| [Bulk Update Documents](actions/bulk-update-documents.md) | PUT | Updates multiple documents in Freshworks CRM. |
| [Bulk Upsert Deals](actions/bulk-upsert-deals.md) | PUT | Finds or creates multiple deals in Freshworks CRM. |
| [Clone Deal](actions/clone-deal.md) | POST | Creates a deal by cloning one in Freshworks CRM. |
| [Create Deal](actions/create-deal.md) | POST | Creates a new deal in Freshworks CRM. |
| [Create Document](actions/create-document.md) | POST | Creates a new document in Freshworks CRM. |
| [Delete Deal](actions/delete-deal.md) | DELETE | Deletes an existing deal from Freshworks CRM. |
| [Delete Document](actions/delete-document.md) | DELETE | Deletes an existing document from Freshworks CRM. |
| [Forget Deal](actions/forget-deal.md) | DELETE | Permanently deletes a deal from Freshworks CRM. |
| [Forget Document](actions/forget-document.md) | DELETE | Permanently deletes a document from Freshworks CRM. |
| [Get Deal](actions/get-deal.md) | GET | Retrieves a deal from Freshworks CRM. |
| [Get Document](actions/get-document.md) | GET | Retrieves a document from Freshworks CRM. |
| [List Deal Fields](actions/list-deal-fields.md) | GET | Retrieves deal fields from Freshworks CRM. |
| [List Deals](actions/list-deals.md) | GET | Retrieves deals from a view in Freshworks CRM. |
| [Manage Deal Products](actions/manage-deal-products.md) | PUT | Updates products on a deal in Freshworks CRM. |
| [Manage Document Products](actions/manage-document-products.md) | PUT | Updates products on a document in Freshworks CRM. |
| [Restore Document](actions/restore-document.md) | PUT | Restores a document in Freshworks CRM. |
| [Update Deal](actions/update-deal.md) | PUT | Updates an existing deal in Freshworks CRM. |
| [Update Deal Team](actions/update-deal-team.md) | PUT | Updates team members for a deal in Freshworks CRM. |
| [Update Document](actions/update-document.md) | PUT | Updates an existing document in Freshworks CRM. |
| [Upsert Deal](actions/upsert-deal.md) | PUT | Finds a deal in Freshworks CRM, or creates one if no match is found. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Create File](actions/create-file.md) | POST | Uploads a file to Freshworks CRM. |
| [Create Link](actions/create-link.md) | POST | Creates a document link in Freshworks CRM. |
| [List Files And Links](actions/list-files-and-links.md) | GET | Retrieves files and links for a contact in Freshworks CRM. |

### Notes

| Action | Method | Description |
| --- | --- | --- |
| [Create Note](actions/create-note.md) | POST | Creates a new note in Freshworks CRM. |
| [Delete Note](actions/delete-note.md) | DELETE | Deletes an existing note from Freshworks CRM. |
| [Update Note](actions/update-note.md) | PUT | Updates an existing note in Freshworks CRM. |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Assign Product Owner](actions/bulk-assign-product-owner.md) | PUT | Updates product owners in Freshworks CRM in bulk. |
| [Bulk Delete Products](actions/bulk-delete-products.md) | DELETE | Deletes multiple products from Freshworks CRM. |
| [Bulk Restore Products](actions/bulk-restore-products.md) | PUT | Restores multiple products in Freshworks CRM. |
| [Bulk Update Products](actions/bulk-update-products.md) | PUT | Updates multiple products in Freshworks CRM. |
| [Create Product](actions/create-product.md) | POST | Creates a new product in Freshworks CRM. |
| [Delete Product](actions/delete-product.md) | DELETE | Deletes an existing product from Freshworks CRM. |
| [Get Product](actions/get-product.md) | GET | Retrieves a product from Freshworks CRM. |
| [Get Related Products](actions/get-related-products.md) | GET | Retrieves related products from Freshworks CRM. |
| [Manage Product Prices](actions/manage-product-prices.md) | PUT | Updates product prices in Freshworks CRM. |
| [Restore Product](actions/restore-product.md) | PUT | Restores a product in Freshworks CRM. |
| [Update Product](actions/update-product.md) | PUT | Updates an existing product in Freshworks CRM. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Appointment](actions/create-appointment.md) | POST | Creates a new appointment in Freshworks CRM. |
| [Create Manual Call Log](actions/create-manual-call-log.md) | POST | Creates a manual call log in Freshworks CRM. |
| [Create Sales Activity](actions/create-sales-activity.md) | POST | Creates a new sales activity in Freshworks CRM. |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Freshworks CRM. |
| [Delete Appointment](actions/delete-appointment.md) | DELETE | Deletes an existing appointment from Freshworks CRM. |
| [Delete Sales Activity](actions/delete-sales-activity.md) | DELETE | Deletes an existing sales activity from Freshworks CRM. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes an existing task from Freshworks CRM. |
| [Get Appointment](actions/get-appointment.md) | GET | Retrieves a appointment from Freshworks CRM. |
| [Get Job Status](actions/get-job-status.md) | GET | Retrieves job status from Freshworks CRM. |
| [Get Sales Activity](actions/get-sales-activity.md) | GET | Retrieves a sales activity from Freshworks CRM. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from Freshworks CRM. |
| [List Appointments](actions/list-appointments.md) | GET | Retrieves all appointments from Freshworks CRM. |
| [List Sales Activities](actions/list-sales-activities.md) | GET | Retrieves sales activities from Freshworks CRM. |
| [List Sales Activity Fields](actions/list-sales-activity-fields.md) | GET | Retrieves sales activity fields from Freshworks CRM. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves all tasks from Freshworks CRM. |
| [Update Appointment](actions/update-appointment.md) | PUT | Updates an existing appointment in Freshworks CRM. |
| [Update Sales Activity](actions/update-sales-activity.md) | PUT | Updates an existing sales activity in Freshworks CRM. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Freshworks CRM. |

