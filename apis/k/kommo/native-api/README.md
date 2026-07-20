# Kommo: Native API Reference

A consolidated summary of Kommo's API configuration and 137 documented operations, with links to official documentation.

- **Official docs:** https://developers.kommo.com/reference
- **API base URL:** `https://{referer}/api/v4`

## Authentication

### OAuth2

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://www.kommo.com/oauth to approve access.
2. Exchange the returned authorization code with a POST request to https://{{credentials.authorizeRequest.referer}}/oauth2/access_token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `crm notifications`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://{{credentials.authorizeRequest.referer}}/oauth2/access_token.

[Official authentication documentation](https://developers.kommo.com/docs/oauth-20)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (maximum 250). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (137 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Accept Incoming Lead](actions/accept-incoming-lead.md) | `POST /leads/unsorted/:uid/accept` | [docs](https://developers.kommo.com/reference/a-cc-ep-ti-nc-om-in-gl-ea-d) |
| [Attach Entity File](actions/attach-entity-file.md) | `PUT /:entity/:entity_id/files` | [docs](https://developers.kommo.com/reference/a-tt-ac-he-nt-it-yf-il-e) |
| [Bulk Update Catalog Custom Fields](actions/bulk-update-catalog-custom-fields.md) | `PATCH /catalogs/:id/custom_fields` | [docs](https://developers.kommo.com/reference/b-ul-ku-pd-at-ec-at-al-og-cu-st-om-fi-el-ds) |
| [Bulk Update Catalog Elements](actions/bulk-update-catalog-elements.md) | `PATCH /catalogs/:list_id/elements` | [docs](https://developers.kommo.com/reference/b-ul-ku-pd-at-ec-at-al-og-el-em-en-ts) |
| [Bulk Update Catalogs](actions/bulk-update-catalogs.md) | `PATCH /catalogs` | [docs](https://developers.kommo.com/reference/b-ul-ku-pd-at-ec-at-al-og-s) |
| [Bulk Update Chat Templates](actions/bulk-update-chat-templates.md) | `PATCH /chats/templates` | [docs](https://developers.kommo.com/reference/b-ul-ku-pd-at-ec-ha-tt-em-pl-at-es) |
| [Bulk Update Companies](actions/bulk-update-companies.md) | `PATCH /companies` | [docs](https://developers.kommo.com/reference/b-ul-ku-pd-at-ec-om-pa-ni-es) |
| [Bulk Update Contacts](actions/bulk-update-contacts.md) | `PATCH /contacts` | [docs](https://developers.kommo.com/reference/b-ul-ku-pd-at-ec-on-ta-ct-s) |
| [Bulk Update Custom Fields](actions/bulk-update-custom-fields.md) | `PATCH /:entity_type/custom_fields` | [docs](https://developers.kommo.com/reference/b-ul-ku-pd-at-ec-us-to-mf-ie-ld-s) |
| [Bulk Update Entity Tags](actions/bulk-update-entity-tags.md) | `PATCH /:entity_type` | [docs](https://developers.kommo.com/reference/b-ul-ku-pd-at-ee-nt-it-yt-ag-s) |
| [Bulk Update Leads](actions/bulk-update-leads.md) | `PATCH /leads` | [docs](https://developers.kommo.com/reference/b-ul-ku-pd-at-el-ea-ds) |
| [Bulk Update Notes](actions/bulk-update-notes.md) | `PATCH /:entity_type/notes` | [docs](https://developers.kommo.com/reference/b-ul-ku-pd-at-en-ot-es) |
| [Bulk Update Sources](actions/bulk-update-sources.md) | `PATCH /sources` | [docs](https://developers.kommo.com/reference/b-ul-ku-pd-at-es-ou-rc-es) |
| [Bulk Update Tasks](actions/bulk-update-tasks.md) | `PATCH /tasks` | [docs](https://developers.kommo.com/reference/b-ul-ku-pd-at-et-as-ks) |
| [Close Talk](actions/close-talk.md) | `POST /talks/:id/close` | [docs](https://developers.kommo.com/reference/c-lo-se-ta-lk) |
| [Continue Salesbot](actions/continue-salesbot.md) | `POST /:bot/:bot_id/continue/:continue_id` | [docs](https://developers.kommo.com/reference/c-on-ti-nu-es-al-es-bo-t) |
| [Create Call](actions/create-call.md) | `POST /calls` | [docs](https://developers.kommo.com/reference/c-re-at-ec-al-l) |
| [Create Catalog](actions/create-catalog.md) | `POST /catalogs` | [docs](https://developers.kommo.com/reference/c-re-at-ec-at-al-og) |
| [Create Catalog Custom Field](actions/create-catalog-custom-field.md) | `POST /catalogs/:list_id/custom_fields` | [docs](https://developers.kommo.com/reference/c-re-at-ec-at-al-og-cu-st-om-fi-el-d) |
| [Create Catalog Element](actions/create-catalog-element.md) | `POST /catalogs/:list_id/elements` | [docs](https://developers.kommo.com/reference/c-re-at-ec-at-al-og-el-em-en-t) |
| [Create Chat Template](actions/create-chat-template.md) | `POST /chats/templates` | [docs](https://developers.kommo.com/reference/c-re-at-ec-ha-tt-em-pl-at-e) |
| [Create Company](actions/create-company.md) | `POST /companies` | [docs](https://developers.kommo.com/reference/add-companies) |
| [Create Complex Lead](actions/create-complex-lead.md) | `POST /leads/complex` | [docs](https://developers.kommo.com/reference/c-re-at-ec-om-pl-ex-le-ad) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://developers.kommo.com/reference/add-contacts) |
| [Create Contact Chat](actions/create-contact-chat.md) | `POST /contacts/chats` | [docs](https://developers.kommo.com/reference/c-re-at-ec-on-ta-ct-ch-at) |
| [Create Custom Field](actions/create-custom-field.md) | `POST /:entity_type/custom_fields` | [docs](https://developers.kommo.com/reference/add-custom-fields) |
| [Create Custom Field Group](actions/create-custom-field-group.md) | `POST /:entity_type/custom_fields/groups` | [docs](https://developers.kommo.com/reference/c-re-at-ec-us-to-mf-ie-ld-gr-ou-p) |
| [Create Event](actions/create-event.md) | `POST /../api/v2/events` | [docs](https://developers.kommo.com/reference/c-re-at-ee-ve-nt) |
| [Create Incoming Call Lead](actions/create-incoming-call-lead.md) | `POST /leads/unsorted/sip` | [docs](https://developers.kommo.com/reference/c-re-at-ei-nc-om-in-gc-al-ll-ea-d) |
| [Create Incoming Form Lead](actions/create-incoming-form-lead.md) | `POST /leads/unsorted/forms` | [docs](https://developers.kommo.com/reference/c-re-at-ei-nc-om-in-gf-or-ml-ea-d) |
| [Create Lead](actions/create-lead.md) | `POST /leads` | [docs](https://developers.kommo.com/reference/adding-leads) |
| [Create Note](actions/create-note.md) | `POST /:entity_type/notes` | [docs](https://developers.kommo.com/reference/add-notes) |
| [Create Pipeline](actions/create-pipeline.md) | `POST /leads/pipelines` | [docs](https://developers.kommo.com/reference/c-re-at-ep-ip-el-in-e) |
| [Create Pipeline Stage](actions/create-pipeline-stage.md) | `POST /leads/pipelines/:pipeline_id/statuses` | [docs](https://developers.kommo.com/reference/c-re-at-ep-ip-el-in-es-ta-ge) |
| [Create Role](actions/create-role.md) | `POST /roles` | [docs](https://developers.kommo.com/reference/c-re-at-er-ol-e) |
| [Create Source](actions/create-source.md) | `POST /sources` | [docs](https://developers.kommo.com/reference/c-re-at-es-ou-rc-e) |
| [Create Tag](actions/create-tag.md) | `POST /:entity_type/tags` | [docs](https://developers.kommo.com/reference/c-re-at-et-ag) |
| [Create Task](actions/create-task.md) | `POST /tasks` | [docs](https://developers.kommo.com/reference/add-tasks) |
| [Create User](actions/create-user.md) | `POST /users` | [docs](https://developers.kommo.com/reference/c-re-at-eu-se-r) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://developers.kommo.com/reference/add-webhooks) |
| [Create Website Button](actions/create-website-button.md) | `POST /website_buttons` | [docs](https://developers.kommo.com/reference/c-re-at-ew-eb-si-te-bu-tt-on) |
| [Create Website Button Online Chat](actions/create-website-button-online-chat.md) | `POST /website_buttons/:source_id/online_chat` | [docs](https://developers.kommo.com/reference/c-re-at-ew-eb-si-te-bu-tt-on-on-li-ne-ch-at) |
| [Decline Incoming Lead](actions/decline-incoming-lead.md) | `DELETE /leads/unsorted/:uid/decline` | [docs](https://developers.kommo.com/reference/d-ec-li-ne-in-co-mi-ng-le-ad) |
| [Delete Chat Template](actions/delete-chat-template.md) | `DELETE /chats/templates/:id` | [docs](https://developers.kommo.com/reference/d-el-et-ec-ha-tt-em-pl-at-e) |
| [Delete Chat Templates](actions/delete-chat-templates.md) | `DELETE /chats/templates` | [docs](https://developers.kommo.com/reference/d-el-et-ec-ha-tt-em-pl-at-es) |
| [Delete Custom Field](actions/delete-custom-field.md) | `DELETE /:entity/custom_fields/:id` | [docs](https://developers.kommo.com/reference/d-el-et-ec-us-to-mf-ie-ld) |
| [Delete Custom Field Group](actions/delete-custom-field-group.md) | `DELETE /:entity_type/custom_fields/groups/:id` | [docs](https://developers.kommo.com/reference/d-el-et-ec-us-to-mf-ie-ld-gr-ou-p) |
| [Delete Pipeline](actions/delete-pipeline.md) | `DELETE /leads/pipelines/:id` | [docs](https://developers.kommo.com/reference/d-el-et-ep-ip-el-in-e) |
| [Delete Pipeline Stage](actions/delete-pipeline-stage.md) | `DELETE /leads/pipelines/:pipeline_id/statuses/:id` | [docs](https://developers.kommo.com/reference/d-el-et-ep-ip-el-in-es-ta-ge) |
| [Delete Role](actions/delete-role.md) | `DELETE /roles/:id` | [docs](https://developers.kommo.com/reference/d-el-et-er-ol-e) |
| [Delete Source](actions/delete-source.md) | `DELETE /sources/:id` | [docs](https://developers.kommo.com/reference/d-el-et-es-ou-rc-e) |
| [Delete Sources](actions/delete-sources.md) | `DELETE /sources` | [docs](https://developers.kommo.com/reference/d-el-et-es-ou-rc-es) |
| [Delete Webhooks](actions/delete-webhooks.md) | `DELETE /webhooks` | [docs](https://developers.kommo.com/reference/d-el-et-ew-eb-ho-ok-s) |
| [Delete Widget](actions/delete-widget.md) | `DELETE /widgets/:widget_code` | [docs](https://developers.kommo.com/reference/d-el-et-ew-id-ge-t) |
| [Detach Entity File](actions/detach-entity-file.md) | `DELETE /:entity/:entity_id/files` | [docs](https://developers.kommo.com/reference/d-et-ac-he-nt-it-yf-il-e) |
| [Get Account](actions/get-account.md) | `GET /account` | [docs](https://developers.kommo.com/reference/account-parameters) |
| [Get Catalog](actions/get-catalog.md) | `GET /catalogs/:id` | [docs](https://developers.kommo.com/reference/g-et-ca-ta-lo-g) |
| [Get Catalog Custom Field](actions/get-catalog-custom-field.md) | `GET /catalogs/:list_id/custom_fields/:custom_field_id` | [docs](https://developers.kommo.com/reference/g-et-ca-ta-lo-gc-us-to-mf-ie-ld) |
| [Get Catalog Element](actions/get-catalog-element.md) | `GET /catalogs/:list_id/elements/:element_id` | [docs](https://developers.kommo.com/reference/g-et-ca-ta-lo-ge-le-me-nt) |
| [Get Chat Template](actions/get-chat-template.md) | `GET /chats/templates/:id` | [docs](https://developers.kommo.com/reference/g-et-ch-at-te-mp-la-te) |
| [Get Company](actions/get-company.md) | `GET /companies/:id` | [docs](https://developers.kommo.com/reference/get-company) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:id` | [docs](https://developers.kommo.com/reference/get-contact) |
| [Get Custom Field](actions/get-custom-field.md) | `GET /:entity_type/custom_fields/:id` | [docs](https://developers.kommo.com/reference/custom-fields-by-id) |
| [Get Custom Field Group](actions/get-custom-field-group.md) | `GET /:entity_type/custom_fields/groups/:id` | [docs](https://developers.kommo.com/reference/g-et-cu-st-om-fi-el-dg-ro-up) |
| [Get Event](actions/get-event.md) | `GET /events/:id` | [docs](https://developers.kommo.com/reference/g-et-ev-en-t) |
| [Get Incoming Lead](actions/get-incoming-lead.md) | `GET /leads/unsorted/:uid` | [docs](https://developers.kommo.com/reference/g-et-in-co-mi-ng-le-ad) |
| [Get Incoming Leads Summary](actions/get-incoming-leads-summary.md) | `GET /leads/unsorted/summary` | [docs](https://developers.kommo.com/reference/g-et-in-co-mi-ng-le-ad-ss-um-ma-ry) |
| [Get Lead](actions/get-lead.md) | `GET /leads/:id` | [docs](https://developers.kommo.com/reference/getting-a-lead-by-its-id) |
| [Get Loss Reason](actions/get-loss-reason.md) | `GET /leads/loss_reasons/:id` | [docs](https://developers.kommo.com/reference/g-et-lo-ss-re-as-on) |
| [Get Note](actions/get-note.md) | `GET /:entity_type/notes/:id` | [docs](https://developers.kommo.com/reference/g-et-no-te) |
| [Get Pipeline](actions/get-pipeline.md) | `GET /leads/pipelines/:id` | [docs](https://developers.kommo.com/reference/get-pipeline-by-id) |
| [Get Pipeline Stage](actions/get-pipeline-stage.md) | `GET /leads/pipelines/:pipeline_id/statuses/:id` | [docs](https://developers.kommo.com/reference/get-stage) |
| [Get Role](actions/get-role.md) | `GET /roles/:id` | [docs](https://developers.kommo.com/reference/g-et-ro-le) |
| [Get Source](actions/get-source.md) | `GET /sources/:id` | [docs](https://developers.kommo.com/reference/g-et-so-ur-ce) |
| [Get Talk](actions/get-talk.md) | `GET /talks/:id` | [docs](https://developers.kommo.com/reference/g-et-ta-lk) |
| [Get Task](actions/get-task.md) | `GET /tasks/:id` | [docs](https://developers.kommo.com/reference/task-id) |
| [Get User](actions/get-user.md) | `GET /users/:id` | [docs](https://developers.kommo.com/reference/g-et-us-er) |
| [Get Website Button](actions/get-website-button.md) | `GET /website_buttons/:source_id` | [docs](https://developers.kommo.com/reference/g-et-we-bs-it-eb-ut-to-n) |
| [Get Widget](actions/get-widget.md) | `GET /widgets/:widget_code` | [docs](https://developers.kommo.com/reference/g-et-wi-dg-et) |
| [Install Widget](actions/install-widget.md) | `POST /widgets/:widget_code` | [docs](https://developers.kommo.com/reference/i-ns-ta-ll-wi-dg-et) |
| [Link Entity](actions/link-entity.md) | `POST /:entity/:entity_id/link` | [docs](https://developers.kommo.com/reference/l-in-ke-nt-it-y) |
| [Link Incoming Lead](actions/link-incoming-lead.md) | `POST /leads/unsorted/:uid/link` | [docs](https://developers.kommo.com/reference/l-in-ki-nc-om-in-gl-ea-d) |
| [List Bots](actions/list-bots.md) | `GET /bots` | [docs](https://developers.kommo.com/reference/l-is-tb-ot-s) |
| [List Catalog Custom Fields](actions/list-catalog-custom-fields.md) | `GET /catalogs/:list_id/custom_fields` | [docs](https://developers.kommo.com/reference/l-is-tc-at-al-og-cu-st-om-fi-el-ds) |
| [List Catalog Elements](actions/list-catalog-elements.md) | `GET /catalogs/:list_id/elements` | [docs](https://developers.kommo.com/reference/l-is-tc-at-al-og-el-em-en-ts) |
| [List Catalogs](actions/list-catalogs.md) | `GET /catalogs` | [docs](https://developers.kommo.com/reference/l-is-tc-at-al-og-s) |
| [List Chat Templates](actions/list-chat-templates.md) | `GET /chats/templates` | [docs](https://developers.kommo.com/reference/l-is-tc-ha-tt-em-pl-at-es) |
| [List Companies](actions/list-companies.md) | `GET /companies` | [docs](https://developers.kommo.com/reference/companies-list) |
| [List Contact Chats](actions/list-contact-chats.md) | `GET /contacts/chats` | [docs](https://developers.kommo.com/reference/l-is-tc-on-ta-ct-ch-at-s) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://developers.kommo.com/reference/contacts-list) |
| [List Custom Field Groups](actions/list-custom-field-groups.md) | `GET /:entity_type/custom_fields/groups` | [docs](https://developers.kommo.com/reference/l-is-tc-us-to-mf-ie-ld-gr-ou-ps) |
| [List Custom Fields](actions/list-custom-fields.md) | `GET /:entity_type/custom_fields` | [docs](https://developers.kommo.com/reference/custom-field-by-entity) |
| [List Entity Files](actions/list-entity-files.md) | `GET /:entity/:entity_id/files` | [docs](https://developers.kommo.com/reference/l-is-te-nt-it-yf-il-es) |
| [List Entity Links](actions/list-entity-links.md) | `GET /:entity/:entity_id/links` | [docs](https://developers.kommo.com/reference/l-is-te-nt-it-yl-in-ks) |
| [List Event Types](actions/list-event-types.md) | `GET /events/types` | [docs](https://developers.kommo.com/reference/l-is-te-ve-nt-ty-pe-s) |
| [List Events](actions/list-events.md) | `GET /events` | [docs](https://developers.kommo.com/reference/l-is-te-ve-nt-s) |
| [List File Links](actions/list-file-links.md) | `GET /files/:file_uuid/links` | [docs](https://developers.kommo.com/reference/l-is-tf-il-el-in-ks) |
| [List Incoming Leads](actions/list-incoming-leads.md) | `GET /leads/unsorted` | [docs](https://developers.kommo.com/reference/l-is-ti-nc-om-in-gl-ea-ds) |
| [List Leads](actions/list-leads.md) | `GET /leads` | [docs](https://developers.kommo.com/reference/leads-list) |
| [List Loss Reasons](actions/list-loss-reasons.md) | `GET /leads/loss_reasons` | [docs](https://developers.kommo.com/reference/l-is-tl-os-sr-ea-so-ns) |
| [List Notes](actions/list-notes.md) | `GET /:entity_type/notes` | [docs](https://developers.kommo.com/reference/l-is-tn-ot-es) |
| [List Notes For Entity](actions/list-notes-for-entity.md) | `GET /:entity_type/:entity_id/notes` | [docs](https://developers.kommo.com/reference/notes-by-entity-id) |
| [List Pipeline Stages](actions/list-pipeline-stages.md) | `GET /leads/pipelines/:pipeline_id/statuses` | [docs](https://developers.kommo.com/reference/stages-list) |
| [List Pipelines](actions/list-pipelines.md) | `GET /leads/pipelines` | [docs](https://developers.kommo.com/reference/pipelines-list) |
| [List Roles](actions/list-roles.md) | `GET /roles` | [docs](https://developers.kommo.com/reference/l-is-tr-ol-es) |
| [List Sources](actions/list-sources.md) | `GET /sources` | [docs](https://developers.kommo.com/reference/l-is-ts-ou-rc-es) |
| [List Tags](actions/list-tags.md) | `GET /:entity_type/tags` | [docs](https://developers.kommo.com/reference/l-is-tt-ag-s) |
| [List Tasks](actions/list-tasks.md) | `GET /tasks` | [docs](https://developers.kommo.com/reference/tasks-list) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://developers.kommo.com/reference/l-is-tu-se-rs) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://developers.kommo.com/reference/list-webhooks) |
| [List Website Buttons](actions/list-website-buttons.md) | `GET /website_buttons` | [docs](https://developers.kommo.com/reference/l-is-tw-eb-si-te-bu-tt-on-s) |
| [List Widgets](actions/list-widgets.md) | `GET /widgets` | [docs](https://developers.kommo.com/reference/l-is-tw-id-ge-ts) |
| [Pin Note](actions/pin-note.md) | `POST /:entity_type/notes/:id/pin` | [docs](https://developers.kommo.com/reference/p-in-no-te) |
| [Run Bot](actions/run-bot.md) | `POST /bots/:id/run` | [docs](https://developers.kommo.com/reference/r-un-bo-t) |
| [Run Bots](actions/run-bots.md) | `POST /bots/run` | [docs](https://developers.kommo.com/reference/r-un-bo-ts) |
| [Run Salesbot](actions/run-salesbot.md) | `POST /../api/v2/salesbot/run` | [docs](https://developers.kommo.com/reference/r-un-sa-le-sb-ot) |
| [Stop Bot](actions/stop-bot.md) | `POST /bots/:id/stop` | [docs](https://developers.kommo.com/reference/s-to-pb-ot) |
| [Submit Chat Template For Review](actions/submit-chat-template-for-review.md) | `POST /chats/templates/:id/review` | [docs](https://developers.kommo.com/reference/s-ub-mi-tc-ha-tt-em-pl-at-ef-or-re-vi-ew) |
| [Unlink Entity](actions/unlink-entity.md) | `POST /:entity/:entity_id/unlink` | [docs](https://developers.kommo.com/reference/u-nl-in-ke-nt-it-y) |
| [Unpin Note](actions/unpin-note.md) | `POST /:entity_type/notes/:id/unpin` | [docs](https://developers.kommo.com/reference/u-np-in-no-te) |
| [Update Catalog](actions/update-catalog.md) | `PATCH /catalogs/:id` | [docs](https://developers.kommo.com/reference/u-pd-at-ec-at-al-og) |
| [Update Catalog Custom Field](actions/update-catalog-custom-field.md) | `PATCH /catalogs/:list_id/custom_fields/:cf_id` | [docs](https://developers.kommo.com/reference/u-pd-at-ec-at-al-og-cu-st-om-fi-el-d) |
| [Update Catalog Element](actions/update-catalog-element.md) | `PATCH /catalogs/:list_id/elements/:element_id` | [docs](https://developers.kommo.com/reference/u-pd-at-ec-at-al-og-el-em-en-t) |
| [Update Chat Template Review](actions/update-chat-template-review.md) | `POST /chats/templates/:id/review/:review_id` | [docs](https://developers.kommo.com/reference/u-pd-at-ec-ha-tt-em-pl-at-er-ev-ie-w) |
| [Update Company](actions/update-company.md) | `PATCH /companies/:id` | [docs](https://developers.kommo.com/reference/updating-company) |
| [Update Contact](actions/update-contact.md) | `PATCH /contacts/:id` | [docs](https://developers.kommo.com/reference/update-contact) |
| [Update Custom Field](actions/update-custom-field.md) | `PATCH /:entity_type/custom_fields/:id` | [docs](https://developers.kommo.com/reference/update-custom-fields) |
| [Update Custom Field Group](actions/update-custom-field-group.md) | `PATCH /:entity_type/custom_fields/groups/:id` | [docs](https://developers.kommo.com/reference/u-pd-at-ec-us-to-mf-ie-ld-gr-ou-p) |
| [Update Entity Tags](actions/update-entity-tags.md) | `PATCH /:entity_type/:id` | [docs](https://developers.kommo.com/reference/u-pd-at-ee-nt-it-yt-ag-s) |
| [Update Lead](actions/update-lead.md) | `PATCH /leads/:id` | [docs](https://developers.kommo.com/reference/updating-single-lead) |
| [Update Note](actions/update-note.md) | `PATCH /:entity_type/notes/:id` | [docs](https://developers.kommo.com/reference/edit-note) |
| [Update Pipeline](actions/update-pipeline.md) | `PATCH /leads/pipelines/:id` | [docs](https://developers.kommo.com/reference/u-pd-at-ep-ip-el-in-e) |
| [Update Pipeline Stage](actions/update-pipeline-stage.md) | `PATCH /leads/pipelines/:pipeline_id/statuses/:id` | [docs](https://developers.kommo.com/reference/u-pd-at-ep-ip-el-in-es-ta-ge) |
| [Update Role](actions/update-role.md) | `PATCH /roles/:id` | [docs](https://developers.kommo.com/reference/u-pd-at-er-ol-e) |
| [Update Source](actions/update-source.md) | `PATCH /sources/:id` | [docs](https://developers.kommo.com/reference/u-pd-at-es-ou-rc-e) |
| [Update Task](actions/update-task.md) | `PATCH /tasks/:id` | [docs](https://developers.kommo.com/reference/edit-task) |
| [Update Website Button](actions/update-website-button.md) | `PATCH /website_buttons/:source_id` | [docs](https://developers.kommo.com/reference/u-pd-at-ew-eb-si-te-bu-tt-on) |
