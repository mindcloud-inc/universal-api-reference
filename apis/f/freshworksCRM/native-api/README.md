# Freshworks CRM: Native API Reference

A consolidated summary of Freshworks CRM's API configuration and 107 documented operations, with links to official documentation.

- **Official docs:** https://developers.freshworks.com/crm/api/
- **API base URL:** `https://{bundleAlias}`

## Authentication

### API Key

Use your Freshworks CRM API key and bundle alias.

### Credentials

- **API Key:** `apiKey` · required
- **Bundle Alias:** `bundleAlias` · optional · Your Freshworks CRM bundle alias without protocol, for example acme.myfreshworks.com/crm/sales.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.freshworks.com/crm/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 25; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (107 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Contacts To List](actions/add-contacts-to-list.md) | `PUT /api/lists/:id/add_contacts` | [docs](https://developers.freshworks.com/crm/api/#add_to_list) |
| [Bulk Assign Contact Owner](actions/bulk-assign-contact-owner.md) | `POST /api/contacts/bulk_assign_owner` | [docs](https://developers.freshworks.com/crm/api/#bulk_assign_contact_owner) |
| [Bulk Assign Document Owner](actions/bulk-assign-document-owner.md) | `POST /api/cpq/cpq_documents/cpq_documents_bulk_assign` | [docs](https://developers.freshworks.com/crm/api/#bulk_assign_document_owner) |
| [Bulk Assign Product Owner](actions/bulk-assign-product-owner.md) | `POST /api/cpq/products/products_bulk_assign` | [docs](https://developers.freshworks.com/crm/api/#bulk_assign_product_owner) |
| [Bulk Delete Accounts](actions/bulk-delete-accounts.md) | `POST /api/sales_accounts/bulk_destroy` | [docs](https://developers.freshworks.com/crm/api/#bulk_delete_account) |
| [Bulk Delete Contacts](actions/bulk-delete-contacts.md) | `POST /api/contacts/bulk_destroy` | [docs](https://developers.freshworks.com/crm/api/#bulk_delete_contact) |
| [Bulk Delete Custom Module Records](actions/bulk-delete-custom-module-records.md) | `POST /api/custom_module/:entity_name/bulk_destroy` | [docs](https://developers.freshworks.com/crm/api/#bulk_delete_records_in_custom_module) |
| [Bulk Delete Deals](actions/bulk-delete-deals.md) | `POST /api/deals/bulk_destroy` | [docs](https://developers.freshworks.com/crm/api/#bulk_delete_deal) |
| [Bulk Delete Documents](actions/bulk-delete-documents.md) | `POST /api/cpq/cpq_documents/cpq_documents_bulk_delete` | [docs](https://developers.freshworks.com/crm/api/#bulk_delete_documents) |
| [Bulk Delete Products](actions/bulk-delete-products.md) | `POST /api/cpq/products/products_bulk_delete` | [docs](https://developers.freshworks.com/crm/api/#bulk_delete_products) |
| [Bulk Restore Documents](actions/bulk-restore-documents.md) | `POST /api/cpq/cpq_documents/cpq_documents_bulk_restore` | [docs](https://developers.freshworks.com/crm/api/#bulk_restore_documents) |
| [Bulk Restore Products](actions/bulk-restore-products.md) | `POST /api/cpq/products/products_bulk_restore` | [docs](https://developers.freshworks.com/crm/api/#bulk_restore_products) |
| [Bulk Update Documents](actions/bulk-update-documents.md) | `PUT /api/cpq/cpq_documents/cpq_documents_bulk_update` | [docs](https://developers.freshworks.com/crm/api/#bulk_update_documents) |
| [Bulk Update Products](actions/bulk-update-products.md) | `PUT /api/cpq/products/products_bulk_update` | [docs](https://developers.freshworks.com/crm/api/#bulk_update_products) |
| [Bulk Upsert Accounts](actions/bulk-upsert-accounts.md) | `POST /api/sales_accounts/bulk_upsert` | [docs](https://developers.freshworks.com/crm/api/#bulk_upsert_account) |
| [Bulk Upsert Contacts](actions/bulk-upsert-contacts.md) | `POST /api/contacts/bulk_upsert` | [docs](https://developers.freshworks.com/crm/api/#bulk_upsert_contact) |
| [Bulk Upsert Deals](actions/bulk-upsert-deals.md) | `POST /api/deals/bulk_upsert` | [docs](https://developers.freshworks.com/crm/api/#bulk_upsert_deal) |
| [Clone Account](actions/clone-account.md) | `POST /api/sales_accounts/:id/clone` | [docs](https://developers.freshworks.com/crm/api/#clone_an_account) |
| [Clone Contact](actions/clone-contact.md) | `POST /api/contacts/:id/clone` | [docs](https://developers.freshworks.com/crm/api/#clone_a_contact) |
| [Clone Custom Module Record](actions/clone-custom-module-record.md) | `POST /api/custom_module/:entity_name/:id/clone` | [docs](https://developers.freshworks.com/crm/api/#clone_record_in_custom_module) |
| [Clone Deal](actions/clone-deal.md) | `POST /api/deals/:id/clone` | [docs](https://developers.freshworks.com/crm/api/#clone_a_deal) |
| [Create Appointment](actions/create-appointment.md) | `POST /api/appointments` | [docs](https://developers.freshworks.com/crm/api/#create_appointment) |
| [Create Contact](actions/create-contact.md) | `POST api/contacts` | [docs](https://developers.freshworks.com/crm/api/#create_contact) |
| [Create Custom Module](actions/create-custom-module.md) | `POST /api/settings/module_customizations` | [docs](https://developers.freshworks.com/crm/api/#create_custom_modules) |
| [Create Custom Module Field](actions/create-custom-module-field.md) | `POST /api/settings/:entity_type/forms/:form_id/fields` | [docs](https://developers.freshworks.com/crm/api/#create_custom_field) |
| [Create Custom Module Record](actions/create-custom-module-record.md) | `POST /api/custom_module/:entity_name` | [docs](https://developers.freshworks.com/crm/api/#create_record_in_custom_module) |
| [Create Deal](actions/create-deal.md) | `POST api/deals` | [docs](https://developers.freshworks.com/crm/api/#create_deal) |
| [Create Document](actions/create-document.md) | `POST /api/cpq/cpq_documents` | [docs](https://developers.freshworks.com/crm/api/#create_document) |
| [Create File](actions/create-file.md) | `POST /api/documents` | [docs](https://developers.freshworks.com/crm/api/#create_file) |
| [Create Link](actions/create-link.md) | `POST /api/document_links` | [docs](https://developers.freshworks.com/crm/api/#create_link) |
| [Create List](actions/create-list.md) | `POST /api/lists` | [docs](https://developers.freshworks.com/crm/api/#create_list) |
| [Create Manual Call Log](actions/create-manual-call-log.md) | `POST /api/phone_calls` | [docs](https://developers.freshworks.com/crm/api/#manual_call_log) |
| [Create Note](actions/create-note.md) | `POST /api/notes` | [docs](https://developers.freshworks.com/crm/api/#create_note) |
| [Create Product](actions/create-product.md) | `POST /api/cpq/products` | [docs](https://developers.freshworks.com/crm/api/#create_product) |
| [Create Sales Account](actions/create-sales-account.md) | `POST api/sales_accounts` | [docs](https://developers.freshworks.com/crm/api/#create_account) |
| [Create Sales Activity](actions/create-sales-activity.md) | `POST /api/sales_activities` | [docs](https://developers.freshworks.com/crm/api/#create_sales_activity) |
| [Create Task](actions/create-task.md) | `POST /api/tasks` | [docs](https://developers.freshworks.com/crm/api/#create_task) |
| [Delete Appointment](actions/delete-appointment.md) | `DELETE /api/appointments/:id` | [docs](https://developers.freshworks.com/crm/api/#delete_an_appointment) |
| [Delete Contact](actions/delete-contact.md) | `DELETE api/contacts/:id` | [docs](https://developers.freshworks.com/crm/api/#delete_a_contact) |
| [Delete Custom Module](actions/delete-custom-module.md) | `DELETE /api/settings/module_customizations/:id` | [docs](https://developers.freshworks.com/crm/api/#delete_custom_module) |
| [Delete Custom Module Record](actions/delete-custom-module-record.md) | `DELETE /api/custom_module/:entity_name/:id` | [docs](https://developers.freshworks.com/crm/api/#delete_record_in_custom_module) |
| [Delete Deal](actions/delete-deal.md) | `DELETE api/deals/:id` | [docs](https://developers.freshworks.com/crm/api/#delete_a_deal) |
| [Delete Document](actions/delete-document.md) | `DELETE /api/cpq/cpq_documents/:id` | [docs](https://developers.freshworks.com/crm/api/#delete_a_document) |
| [Delete Note](actions/delete-note.md) | `DELETE /api/notes/:id` | [docs](https://developers.freshworks.com/crm/api/#delete_a_note) |
| [Delete Product](actions/delete-product.md) | `DELETE /api/cpq/products/:id` | [docs](https://developers.freshworks.com/crm/api/#delete_a_product) |
| [Delete Sales Account](actions/delete-sales-account.md) | `DELETE api/sales_accounts/:id` | [docs](https://developers.freshworks.com/crm/api/#delete_account) |
| [Delete Sales Activity](actions/delete-sales-activity.md) | `DELETE /api/sales_activities/:id` | [docs](https://developers.freshworks.com/crm/api/#delete_a_sales_activity) |
| [Delete Task](actions/delete-task.md) | `DELETE /api/tasks/:id` | [docs](https://developers.freshworks.com/crm/api/#delete_task) |
| [Forget Account](actions/forget-account.md) | `DELETE /api/sales_accounts/:id/forget` | [docs](https://developers.freshworks.com/crm/api/#forget_account) |
| [Forget Contact](actions/forget-contact.md) | `DELETE /api/contacts/:id/forget` | [docs](https://developers.freshworks.com/crm/api/#forget_a_contact) |
| [Forget Custom Module Record](actions/forget-custom-module-record.md) | `DELETE /api/custom_module/:entity_name/:id/forget` | [docs](https://developers.freshworks.com/crm/api/#forget_record_in_custom_module) |
| [Forget Deal](actions/forget-deal.md) | `DELETE /api/deals/:id/forget` | [docs](https://developers.freshworks.com/crm/api/#forget_a_deal) |
| [Forget Document](actions/forget-document.md) | `DELETE /api/cpq/cpq_documents/:id/forget` | [docs](https://developers.freshworks.com/crm/api/#forget_a_document) |
| [Get Appointment](actions/get-appointment.md) | `GET /api/appointments/:id` | [docs](https://developers.freshworks.com/crm/api/#view_an_appointment) |
| [Get Contact](actions/get-contact.md) | `GET api/contacts/:id` | [docs](https://developers.freshworks.com/crm/api/#view_a_contact) |
| [Get Custom Module](actions/get-custom-module.md) | `GET /api/settings/module_customizations/:id` | [docs](https://developers.freshworks.com/crm/api/#get_list_of_custom_modules) |
| [Get Custom Module Record](actions/get-custom-module-record.md) | `GET /api/custom_module/:entity_name/:id` | [docs](https://developers.freshworks.com/crm/api/#get_list_of_all_records_in_custom_module) |
| [Get Deal](actions/get-deal.md) | `GET api/deals/:id` | [docs](https://developers.freshworks.com/crm/api/#view_a_deal) |
| [Get Document](actions/get-document.md) | `GET /api/cpq/cpq_documents/:id` | [docs](https://developers.freshworks.com/crm/api/#view_a_document) |
| [Get Job Status](actions/get-job-status.md) | `GET /api/job_statuses/:id` | [docs](https://developers.freshworks.com/crm/api/#job_status_api) |
| [Get Product](actions/get-product.md) | `GET /api/cpq/products/:id` | [docs](https://developers.freshworks.com/crm/api/#view_a_product) |
| [Get Related Products](actions/get-related-products.md) | `GET /api/cpq/cpq_documents/:id/related_products` | [docs](https://developers.freshworks.com/crm/api/#related_products) |
| [Get Sales Account](actions/get-sales-account.md) | `GET api/sales_accounts/:id` | [docs](https://developers.freshworks.com/crm/api/#view_account) |
| [Get Sales Activity](actions/get-sales-activity.md) | `GET /api/sales_activities/:id` | [docs](https://developers.freshworks.com/crm/api/#view_a_sales_activity) |
| [Get Task](actions/get-task.md) | `GET /api/tasks/:id` | [docs](https://developers.freshworks.com/crm/api/#view_task) |
| [List Appointments](actions/list-appointments.md) | `GET /api/appointments` | [docs](https://developers.freshworks.com/crm/api/#list_all_appointment) |
| [List Contact Activities](actions/list-contact-activities.md) | `GET /api/contacts/:id/activities` | [docs](https://developers.freshworks.com/crm/api/#list_all_contact_activities) |
| [List Contact Fields](actions/list-contact-fields.md) | `GET api/settings/contacts/fields` | [docs](https://developers.freshworks.com/crm/api/#list_all_contact_fields) |
| [List Contacts](actions/list-contacts.md) | `GET api/contacts/view/:view_id` | [docs](https://developers.freshworks.com/crm/api/#list_all_contacts) |
| [List Contacts In List](actions/list-contacts-in-list.md) | `GET /api/contacts/lists/:id` | [docs](https://developers.freshworks.com/crm/api/#fetch_all_contacts_from_list) |
| [List Custom Module Fields](actions/list-custom-module-fields.md) | `GET /api/settings/:entity_type/forms` | [docs](https://developers.freshworks.com/crm/api/#list_of_all_fields_in_your_custom_module) |
| [List Deal Fields](actions/list-deal-fields.md) | `GET api/settings/deals/fields` | [docs](https://developers.freshworks.com/crm/api/#list_all_deal_fields) |
| [List Deals](actions/list-deals.md) | `GET api/deals/view/:view_id` | [docs](https://developers.freshworks.com/crm/api/#list_all_deals) |
| [List Files And Links](actions/list-files-and-links.md) | `GET /api/contacts/:id/document_associations` | [docs](https://developers.freshworks.com/crm/api/#list_files) |
| [List Lists](actions/list-lists.md) | `GET /api/lists` | [docs](https://developers.freshworks.com/crm/api/#fetch_all_lists) |
| [List Sales Account Fields](actions/list-sales-account-fields.md) | `GET api/settings/sales_accounts/fields` | [docs](https://developers.freshworks.com/crm/api/#list_all_account_fields) |
| [List Sales Accounts](actions/list-sales-accounts.md) | `GET api/sales_accounts/view/:view_id` | [docs](https://developers.freshworks.com/crm/api/#list_all_accounts) |
| [List Sales Activities](actions/list-sales-activities.md) | `GET api/sales_activities` | [docs](https://developers.freshworks.com/crm/api/#list_all_sales_activities) |
| [List Sales Activity Fields](actions/list-sales-activity-fields.md) | `GET /api/settings/sales_activities/fields` | [docs](https://developers.freshworks.com/crm/api/#list_all_sales_activity_fields) |
| [List Tasks](actions/list-tasks.md) | `GET /api/tasks` | [docs](https://developers.freshworks.com/crm/api/#list_all_task) |
| [Lookup Search](actions/lookup-search.md) | `GET /api/lookup` | [docs](https://developers.freshworks.com/crm/api/#lookup_search) |
| [Manage Deal Products](actions/manage-deal-products.md) | `PUT /api/deals/:id` | [docs](https://developers.freshworks.com/crm/api/#add_products_to_the_deal) |
| [Manage Document Products](actions/manage-document-products.md) | `PUT /api/cpq/cpq_documents/:id` | [docs](https://developers.freshworks.com/crm/api/#add_products_to_the_document) |
| [Manage Product Prices](actions/manage-product-prices.md) | `PUT /api/cpq/products/:id` | [docs](https://developers.freshworks.com/crm/api/#add_prices_to_the_product) |
| [Move Contacts Between Lists](actions/move-contacts-between-lists.md) | `PUT /api/lists/:id/move_contacts` | [docs](https://developers.freshworks.com/crm/api/#move_contact_from_list) |
| [Remove Contacts From List](actions/remove-contacts-from-list.md) | `PUT /api/lists/:id/remove_contacts` | [docs](https://developers.freshworks.com/crm/api/#remove_contact_from_list) |
| [Restore Document](actions/restore-document.md) | `PUT /api/cpq/cpq_documents/:id/restore` | [docs](https://developers.freshworks.com/crm/api/#restore_a_document) |
| [Restore Product](actions/restore-product.md) | `PUT /api/cpq/products/:id/restore` | [docs](https://developers.freshworks.com/crm/api/#restore_a_product) |
| [Search Records](actions/search-records.md) | `GET api/search` | [docs](https://developers.freshworks.com/crm/api/#search) |
| [Update Account Team](actions/update-account-team.md) | `POST /api/sales_accounts/:id/manage_team_members` | [docs](https://developers.freshworks.com/crm/api/#update_account_team) |
| [Update Appointment](actions/update-appointment.md) | `PUT /api/appointments/:id` | [docs](https://developers.freshworks.com/crm/api/#update_an_appointment) |
| [Update Contact](actions/update-contact.md) | `PUT api/contacts/:id` | [docs](https://developers.freshworks.com/crm/api/#update_a_contact) |
| [Update Contact Team](actions/update-contact-team.md) | `POST /api/contacts/:id/manage_team_members` | [docs](https://developers.freshworks.com/crm/api/#update_contact_team) |
| [Update Custom Module](actions/update-custom-module.md) | `PUT /api/settings/module_customizations/:id` | [docs](https://developers.freshworks.com/crm/api/#update_custom_module) |
| [Update Custom Module Record](actions/update-custom-module-record.md) | `PUT /api/custom_module/:entity_name/:id` | [docs](https://developers.freshworks.com/crm/api/#update_record_in_custom_module) |
| [Update Deal](actions/update-deal.md) | `PUT api/deals/:id` | [docs](https://developers.freshworks.com/crm/api/#update_a_deal) |
| [Update Deal Team](actions/update-deal-team.md) | `POST /api/deals/:id/manage_team_members` | [docs](https://developers.freshworks.com/crm/api/#update_deal_team) |
| [Update Document](actions/update-document.md) | `PUT /api/cpq/cpq_documents/:id` | [docs](https://developers.freshworks.com/crm/api/#update_a_document) |
| [Update List](actions/update-list.md) | `PUT /api/lists/:id` | [docs](https://developers.freshworks.com/crm/api/#update_a_list) |
| [Update Note](actions/update-note.md) | `PUT /api/notes/:id` | [docs](https://developers.freshworks.com/crm/api/#update_note) |
| [Update Product](actions/update-product.md) | `PUT /api/cpq/products/:id` | [docs](https://developers.freshworks.com/crm/api/#update_a_product) |
| [Update Sales Account](actions/update-sales-account.md) | `PUT api/sales_accounts/:id` | [docs](https://developers.freshworks.com/crm/api/#update_a_account) |
| [Update Sales Activity](actions/update-sales-activity.md) | `PUT /api/sales_activities/:id` | [docs](https://developers.freshworks.com/crm/api/#update_a_sales_activity) |
| [Update Task](actions/update-task.md) | `PUT /api/tasks/:id` | [docs](https://developers.freshworks.com/crm/api/#update_task) |
| [Upsert Account](actions/upsert-account.md) | `POST /api/sales_accounts/upsert` | [docs](https://developers.freshworks.com/crm/api/#upsert_an_account) |
| [Upsert Contact](actions/upsert-contact.md) | `POST /api/contacts/upsert` | [docs](https://developers.freshworks.com/crm/api/#upsert_a_contact) |
| [Upsert Deal](actions/upsert-deal.md) | `POST /api/deals/upsert` | [docs](https://developers.freshworks.com/crm/api/#upsert_a_deal) |
