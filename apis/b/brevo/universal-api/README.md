# <img src="https://images.mindcloud.co/apps/icons/brevo_1772485569892.png" alt="Brevo logo" width="28" height="28"> Brevo: Universal API

Manage contacts, automate campaigns, send messages, and grow customer relationships.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/brevo/latest
- **Category:** Marketing
- **Actions:** 285
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.brevo.com
- **Vendor API docs:** https://developers.brevo.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/brevo/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (285)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET |  |

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Create SMS Campaign](actions/create-sms-campaign.md) | POST |  |
| [Create WhatsApp Campaign](actions/create-whats-app-campaign.md) | POST |  |
| [Create WhatsApp Template](actions/create-whats-app-template.md) | POST |  |
| [Delete Email Campaign](actions/delete-email-campaign.md) | DELETE |  |
| [Delete SMS Campaign](actions/delete-sms-campaign.md) | DELETE |  |
| [Delete WhatsApp Campaign](actions/delete-whats-app-campaign.md) | DELETE |  |
| [Export Email Campaign Recipients](actions/export-email-campaign-recipients.md) | POST |  |
| [Export SMS Campaign Recipients](actions/export-sms-campaign-recipients.md) | POST |  |
| [Get Email Campaign AB Test Result](actions/get-email-campaign-ab-test-result.md) | GET |  |
| [Get Email Campaign Shared URL](actions/get-email-campaign-shared-url.md) | GET |  |
| [Get SMS Campaign](actions/get-sms-campaign.md) | GET |  |
| [Get WhatsApp Campaign](actions/get-whats-app-campaign.md) | GET |  |
| [Get WhatsApp Campaign Config](actions/get-whats-app-campaign-config.md) | GET |  |
| [List SMS Campaigns](actions/list-sms-campaigns.md) | GET |  |
| [List SMS Templates](actions/list-sms-templates.md) | GET |  |
| [List WhatsApp Campaigns](actions/list-whats-app-campaigns.md) | GET |  |
| [List WhatsApp Templates](actions/list-whats-app-templates.md) | GET |  |
| [Send Async Transactional SMS](actions/send-async-transactional-sms.md) | POST |  |
| [Send Email Campaign Now](actions/send-email-campaign-now.md) | POST |  |
| [Send Email Campaign Report](actions/send-email-campaign-report.md) | POST |  |
| [Send Email Campaign Test](actions/send-email-campaign-test.md) | POST |  |
| [Send SMS Campaign Now](actions/send-sms-campaign-now.md) | POST |  |
| [Send SMS Campaign Report](actions/send-sms-campaign-report.md) | POST |  |
| [Send SMS Campaign Test](actions/send-sms-campaign-test.md) | POST |  |
| [Send Transactional SMS](actions/send-transactional-sms.md) | POST |  |
| [Send WhatsApp Message](actions/send-whats-app-message.md) | POST |  |
| [Send WhatsApp Template Approval](actions/send-whats-app-template-approval.md) | POST |  |
| [Update Email Campaign Status](actions/update-email-campaign-status.md) | PUT |  |
| [Update SMS Campaign](actions/update-sms-campaign.md) | PUT |  |
| [Update SMS Campaign Status](actions/update-sms-campaign-status.md) | PUT |  |
| [Update WhatsApp Campaign](actions/update-whats-app-campaign.md) | PUT |  |
| [Upload Email Campaign Image](actions/upload-email-campaign-image.md) | POST |  |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [Create Categories Batch](actions/create-categories-batch.md) | POST |  |
| [Create Category](actions/create-category.md) | POST |  |

### Collections

| Action | Method | Description |
| --- | --- | --- |
| [Create Coupon Collection](actions/create-coupon-collection.md) | POST |  |
| [Create Coupons](actions/create-coupons.md) | POST |  |
| [Update Coupon Collection](actions/update-coupon-collection.md) | PUT |  |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Assign Loyalty Tier](actions/assign-loyalty-tier.md) | POST |  |
| [Associate Corporate Sub Account IP](actions/associate-corporate-sub-account-ip.md) | POST |  |
| [Cancel Loyalty Transaction](actions/cancel-loyalty-transaction.md) | POST |  |
| [Complete Loyalty Redeem Transaction](actions/complete-loyalty-redeem-transaction.md) | POST |  |
| [Complete Loyalty Transaction](actions/complete-loyalty-transaction.md) | POST |  |
| [Create Company](actions/create-company.md) | POST |  |
| [Create Corporate Group](actions/create-corporate-group.md) | POST |  |
| [Create Corporate Sub Account](actions/create-corporate-sub-account.md) | POST |  |
| [Create Corporate Sub Account API Key](actions/create-corporate-sub-account-api-key.md) | POST |  |
| [Create CRM Attribute](actions/create-crm-attribute.md) | POST |  |
| [Create Loyalty Balance Definition](actions/create-loyalty-balance-definition.md) | POST |  |
| [Create Loyalty Balance Limit](actions/create-loyalty-balance-limit.md) | POST |  |
| [Create Loyalty Order](actions/create-loyalty-order.md) | POST |  |
| [Create Loyalty Program](actions/create-loyalty-program.md) | POST |  |
| [Create Loyalty Reward](actions/create-loyalty-reward.md) | POST |  |
| [Create Loyalty Subscription Balances](actions/create-loyalty-subscription-balances.md) | POST |  |
| [Create Loyalty Subscription Member](actions/create-loyalty-subscription-member.md) | POST |  |
| [Create Loyalty Tier](actions/create-loyalty-tier.md) | POST |  |
| [Create Loyalty Tier Group](actions/create-loyalty-tier-group.md) | POST |  |
| [Create Loyalty Transaction](actions/create-loyalty-transaction.md) | POST |  |
| [Create Loyalty Voucher](actions/create-loyalty-voucher.md) | POST |  |
| [Delete Company](actions/delete-company.md) | DELETE |  |
| [Delete Corporate Group](actions/delete-corporate-group.md) | DELETE |  |
| [Delete Corporate Sub Account](actions/delete-corporate-sub-account.md) | DELETE |  |
| [Delete CRM Attribute](actions/delete-crm-attribute.md) | DELETE |  |
| [Delete Loyalty Balance Definition](actions/delete-loyalty-balance-definition.md) | DELETE |  |
| [Delete Loyalty Balance Limit](actions/delete-loyalty-balance-limit.md) | DELETE |  |
| [Delete Loyalty Contact Subscription](actions/delete-loyalty-contact-subscription.md) | DELETE |  |
| [Delete Loyalty Program](actions/delete-loyalty-program.md) | DELETE |  |
| [Delete Loyalty Subscription Members](actions/delete-loyalty-subscription-members.md) | DELETE |  |
| [Delete Loyalty Tier](actions/delete-loyalty-tier.md) | DELETE |  |
| [Delete Loyalty Tier Group](actions/delete-loyalty-tier-group.md) | DELETE |  |
| [Dissociate Corporate Sub Account IP](actions/dissociate-corporate-sub-account-ip.md) | PUT |  |
| [Get Company](actions/get-company.md) | GET |  |
| [Get Corporate Group](actions/get-corporate-group.md) | GET |  |
| [Get Corporate Sub Account](actions/get-corporate-sub-account.md) | GET |  |
| [Get Loyalty Active Balances](actions/get-loyalty-active-balances.md) | GET |  |
| [Get Loyalty Balance Definition](actions/get-loyalty-balance-definition.md) | GET |  |
| [Get Loyalty Balance Limit](actions/get-loyalty-balance-limit.md) | GET |  |
| [Get Loyalty Code Count](actions/get-loyalty-code-count.md) | GET |  |
| [Get Loyalty Offers](actions/get-loyalty-offers.md) | GET |  |
| [Get Loyalty Program](actions/get-loyalty-program.md) | GET |  |
| [Get Loyalty Programs](actions/get-loyalty-programs.md) | GET |  |
| [Get Loyalty Reward](actions/get-loyalty-reward.md) | GET |  |
| [Get Loyalty Subscription Balances](actions/get-loyalty-subscription-balances.md) | GET |  |
| [Get Loyalty Subscription Data](actions/get-loyalty-subscription-data.md) | GET |  |
| [Get Loyalty Tier Group](actions/get-loyalty-tier-group.md) | GET |  |
| [Get Loyalty Vouchers](actions/get-loyalty-vouchers.md) | GET |  |
| [Get Master Account](actions/get-master-account.md) | GET |  |
| [Import Companies](actions/import-companies.md) | POST |  |
| [Link Unlink Company](actions/link-unlink-company.md) | PUT |  |
| [List Companies](actions/list-companies.md) | GET |  |
| [List Corporate Groups](actions/list-corporate-groups.md) | GET |  |
| [List Corporate IPs](actions/list-corporate-i-ps.md) | GET |  |
| [List Corporate Sub Accounts](actions/list-corporate-sub-accounts.md) | GET |  |
| [List CRM Company Attributes](actions/list-crm-company-attributes.md) | GET |  |
| [List Loyalty Balance Definitions](actions/list-loyalty-balance-definitions.md) | GET |  |
| [List Loyalty Contact Balances](actions/list-loyalty-contact-balances.md) | GET |  |
| [List Loyalty Tier Groups](actions/list-loyalty-tier-groups.md) | GET |  |
| [List Loyalty Tiers](actions/list-loyalty-tiers.md) | GET |  |
| [List Loyalty Transaction History](actions/list-loyalty-transaction-history.md) | GET |  |
| [Partially Update Loyalty Program](actions/partially-update-loyalty-program.md) | PUT |  |
| [Publish Loyalty Program](actions/publish-loyalty-program.md) | POST |  |
| [Redeem Loyalty Voucher](actions/redeem-loyalty-voucher.md) | POST |  |
| [Revoke Loyalty Vouchers](actions/revoke-loyalty-vouchers.md) | DELETE |  |
| [Subscribe Loyalty Program](actions/subscribe-loyalty-program.md) | POST |  |
| [Toggle Corporate Sub Account Applications](actions/toggle-corporate-sub-account-applications.md) | PUT |  |
| [Unlink Corporate Group Sub Accounts](actions/unlink-corporate-group-sub-accounts.md) | PUT |  |
| [Update Company](actions/update-company.md) | PUT |  |
| [Update Corporate Group](actions/update-corporate-group.md) | PUT |  |
| [Update Corporate Sub Account Plan](actions/update-corporate-sub-account-plan.md) | PUT |  |
| [Update Corporate Sub Accounts Plan](actions/update-corporate-sub-accounts-plan.md) | PUT |  |
| [Update CRM Attribute](actions/update-crm-attribute.md) | PUT |  |
| [Update Ecommerce Display Currency](actions/update-ecommerce-display-currency.md) | PUT |  |
| [Update Loyalty Balance Definition](actions/update-loyalty-balance-definition.md) | PUT |  |
| [Update Loyalty Balance Limit](actions/update-loyalty-balance-limit.md) | PUT |  |
| [Update Loyalty Program](actions/update-loyalty-program.md) | PUT |  |
| [Update Loyalty Tier](actions/update-loyalty-tier.md) | PUT |  |
| [Update Loyalty Tier Group](actions/update-loyalty-tier-group.md) | PUT |  |
| [Validate Loyalty Reward](actions/validate-loyalty-reward.md) | POST |  |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST |  |
| [Delete Contact](actions/delete-contact.md) | DELETE |  |
| [Get Contact](actions/get-contact.md) | GET |  |
| [List Contacts](actions/list-contacts.md) | GET |  |
| [Update Contact](actions/update-contact.md) | PUT |  |

### Contact Attribute

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact Attribute](actions/create-contact-attribute.md) | POST |  |
| [List Contact Attributes](actions/list-contact-attributes.md) | GET |  |
| [Update Contact Attribute](actions/update-contact-attribute.md) | PUT |  |

### Contact Export

| Action | Method | Description |
| --- | --- | --- |
| [Export Contacts](actions/export-contacts.md) | POST |  |

### Contact Import

| Action | Method | Description |
| --- | --- | --- |
| [Import Contacts](actions/import-contacts.md) | POST |  |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contacts Batch](actions/create-contacts-batch.md) | POST |  |
| [Delete Contact Attribute](actions/delete-contact-attribute.md) | DELETE |  |
| [Delete Contact Attribute Option](actions/delete-contact-attribute-option.md) | DELETE |  |
| [Get Contact Campaign Stats](actions/get-contact-campaign-stats.md) | GET |  |
| [Send Double Opt-In Confirmation](actions/send-double-opt-in-confirmation.md) | POST |  |

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [Create Conversation Message](actions/create-conversation-message.md) | POST |  |
| [Create Pushed Conversation Message](actions/create-pushed-conversation-message.md) | POST |  |
| [Delete Conversation Message](actions/delete-conversation-message.md) | DELETE |  |
| [Delete Pushed Conversation Message](actions/delete-pushed-conversation-message.md) | DELETE |  |
| [Get Conversation Message](actions/get-conversation-message.md) | GET |  |
| [Get Pushed Conversation Message](actions/get-pushed-conversation-message.md) | GET |  |
| [Ping Conversation Agent Online](actions/ping-conversation-agent-online.md) | POST |  |
| [Update Conversation Message](actions/update-conversation-message.md) | PUT |  |
| [Update Conversation Visitor Group](actions/update-conversation-visitor-group.md) | PUT |  |
| [Update Pushed Conversation Message](actions/update-pushed-conversation-message.md) | PUT |  |

### Deals

| Action | Method | Description |
| --- | --- | --- |
| [Create Deal](actions/create-deal.md) | POST |  |
| [Delete Deal](actions/delete-deal.md) | DELETE |  |
| [Get CRM Pipeline](actions/get-crm-pipeline.md) | GET |  |
| [Get Deal](actions/get-deal.md) | GET |  |
| [Import Deals](actions/import-deals.md) | POST |  |
| [Link Unlink Deal](actions/link-unlink-deal.md) | PUT |  |
| [List CRM Deal Attributes](actions/list-crm-deal-attributes.md) | GET |  |
| [List CRM Pipelines](actions/list-crm-pipelines.md) | GET |  |
| [List Deals](actions/list-deals.md) | GET |  |
| [Update Deal](actions/update-deal.md) | PUT |  |

### Email Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Create Email Campaign](actions/create-email-campaign.md) | POST |  |
| [Get Email Campaign](actions/get-email-campaign.md) | GET |  |
| [List Email Campaigns](actions/list-email-campaigns.md) | GET |  |
| [Update Email Campaign](actions/update-email-campaign.md) | PUT |  |

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Authenticate Sender Domain](actions/authenticate-sender-domain.md) | PUT |  |
| [Create Blocked Domain](actions/create-blocked-domain.md) | POST |  |
| [Create Sender](actions/create-sender.md) | POST |  |
| [Create Sender Domain](actions/create-sender-domain.md) | POST |  |
| [Delete Blocked Contact](actions/delete-blocked-contact.md) | DELETE |  |
| [Delete Blocked Domain](actions/delete-blocked-domain.md) | DELETE |  |
| [Delete Hard Bounces](actions/delete-hard-bounces.md) | POST |  |
| [Delete Scheduled Email](actions/delete-scheduled-email.md) | DELETE |  |
| [Delete Sender](actions/delete-sender.md) | DELETE |  |
| [Delete Sender Domain](actions/delete-sender-domain.md) | DELETE |  |
| [Delete SMTP Log](actions/delete-smtp-log.md) | DELETE |  |
| [Get Scheduled Email](actions/get-scheduled-email.md) | GET |  |
| [Get Sender Domain](actions/get-sender-domain.md) | GET |  |
| [Get Transactional Email Content](actions/get-transactional-email-content.md) | GET |  |
| [List Blocked Contacts](actions/list-blocked-contacts.md) | GET |  |
| [List Blocked Domains](actions/list-blocked-domains.md) | GET |  |
| [List Sender Domains](actions/list-sender-domains.md) | GET |  |
| [List Sender IPs](actions/list-sender-i-ps.md) | GET |  |
| [List Sender IPs by Sender](actions/list-sender-i-ps-by-sender.md) | GET |  |
| [List Senders](actions/list-senders.md) | GET |  |
| [Preview SMTP Template](actions/preview-smtp-template.md) | POST |  |
| [Send SMTP Template Test](actions/send-smtp-template-test.md) | POST |  |
| [Send Transactional Email](actions/send-transactional-email.md) | POST |  |
| [Update Sender](actions/update-sender.md) | PUT |  |
| [Validate Sender](actions/validate-sender.md) | PUT |  |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Create Event](actions/create-event.md) | POST |  |
| [Create Events Batch](actions/create-events-batch.md) | POST |  |
| [Export Webhook History](actions/export-webhook-history.md) | POST |  |
| [Get Inbound Event](actions/get-inbound-event.md) | GET |  |
| [List Events](actions/list-events.md) | GET |  |
| [List Inbound Events](actions/list-inbound-events.md) | GET |  |
| [List WhatsApp Events](actions/list-whats-app-events.md) | GET |  |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Create CRM File](actions/create-crm-file.md) | POST |  |
| [Create Feed](actions/create-feed.md) | POST |  |
| [Delete CRM File](actions/delete-crm-file.md) | DELETE |  |
| [Delete Feed](actions/delete-feed.md) | DELETE |  |
| [Get CRM File](actions/get-crm-file.md) | GET |  |
| [Get CRM File Metadata](actions/get-crm-file-metadata.md) | GET |  |
| [Get Feed](actions/get-feed.md) | GET |  |
| [Get Inbound Attachment](actions/get-inbound-attachment.md) | GET |  |
| [List CRM Files](actions/list-crm-files.md) | GET |  |
| [List Feeds](actions/list-feeds.md) | GET |  |
| [Update Feed](actions/update-feed.md) | PUT |  |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact Folder](actions/create-contact-folder.md) | POST |  |
| [Delete Contact Folder](actions/delete-contact-folder.md) | DELETE |  |
| [Get Contact Folder](actions/get-contact-folder.md) | GET |  |
| [List Contact Folders](actions/list-contact-folders.md) | GET |  |
| [List Lists in Folder](actions/list-lists-in-folder.md) | GET |  |
| [Update Contact Folder](actions/update-contact-folder.md) | PUT |  |

### List

| Action | Method | Description |
| --- | --- | --- |
| [Create List](actions/create-list.md) | POST |  |
| [Delete List](actions/delete-list.md) | DELETE |  |
| [Get List](actions/get-list.md) | GET |  |
| [List Lists](actions/list-lists.md) | GET |  |
| [Update List](actions/update-list.md) | PUT |  |

### List Contact

| Action | Method | Description |
| --- | --- | --- |
| [List Contacts in List](actions/list-contacts-in-list.md) | GET |  |

### List Membership

| Action | Method | Description |
| --- | --- | --- |
| [Add Contacts to List](actions/add-contacts-to-list.md) | POST |  |
| [Remove Contacts from List](actions/remove-contacts-from-list.md) | DELETE |  |

### Notes

| Action | Method | Description |
| --- | --- | --- |
| [Create CRM Note](actions/create-crm-note.md) | POST |  |
| [Delete CRM Note](actions/delete-crm-note.md) | DELETE |  |
| [Get CRM Note](actions/get-crm-note.md) | GET |  |
| [List CRM Notes](actions/list-crm-notes.md) | GET |  |
| [Update CRM Note](actions/update-crm-note.md) | PUT |  |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [Activate Ecommerce](actions/activate-ecommerce.md) | POST |  |
| [Create Order Status](actions/create-order-status.md) | POST |  |
| [Create Orders Batch](actions/create-orders-batch.md) | POST |  |
| [Create Payment Request](actions/create-payment-request.md) | POST |  |
| [Delete Payment Request](actions/delete-payment-request.md) | DELETE |  |
| [Get Ecommerce Attribution Metric Detail](actions/get-ecommerce-attribution-metric-detail.md) | GET |  |
| [Get Ecommerce Display Currency](actions/get-ecommerce-display-currency.md) | GET |  |
| [Get Payment Request](actions/get-payment-request.md) | GET |  |
| [List Ecommerce Attribution Metrics](actions/list-ecommerce-attribution-metrics.md) | GET |  |
| [List Orders](actions/list-orders.md) | GET |  |

### Pipelines

| Action | Method | Description |
| --- | --- | --- |
| [List CRM Pipeline Details](actions/list-crm-pipeline-details.md) | GET |  |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Create Product](actions/create-product.md) | POST |  |
| [Create Product Alert](actions/create-product-alert.md) | POST |  |
| [Create Products Batch](actions/create-products-batch.md) | POST |  |
| [Get Category](actions/get-category.md) | GET |  |
| [Get Coupon Collection](actions/get-coupon-collection.md) | GET |  |
| [Get Product](actions/get-product.md) | GET |  |
| [List Categories](actions/list-categories.md) | GET |  |
| [List Coupon Collections](actions/list-coupon-collections.md) | GET |  |
| [List Ecommerce Attributed Products](actions/list-ecommerce-attributed-products.md) | GET |  |
| [List Products](actions/list-products.md) | GET |  |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get SMTP Aggregated Report](actions/get-smtp-aggregated-report.md) | GET |  |
| [Get Transactional SMS Aggregated Report](actions/get-transactional-sms-aggregated-report.md) | GET |  |
| [List SMTP Events](actions/list-smtp-events.md) | GET |  |
| [List SMTP Reports](actions/list-smtp-reports.md) | GET |  |
| [List Transactional SMS Events](actions/list-transactional-sms-events.md) | GET |  |
| [List Transactional SMS Reports](actions/list-transactional-sms-reports.md) | GET |  |

### Segment

| Action | Method | Description |
| --- | --- | --- |
| [List Segments](actions/list-segments.md) | GET |  |

### Smtp Template

| Action | Method | Description |
| --- | --- | --- |
| [Create SMTP Template](actions/create-smtp-template.md) | POST |  |
| [Delete SMTP Template](actions/delete-smtp-template.md) | DELETE |  |
| [Get SMTP Template](actions/get-smtp-template.md) | GET |  |
| [List SMTP Templates](actions/list-smtp-templates.md) | GET |  |
| [Update SMTP Template](actions/update-smtp-template.md) | PUT |  |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create CRM Task](actions/create-crm-task.md) | POST |  |
| [Delete CRM Task](actions/delete-crm-task.md) | DELETE |  |
| [Get CRM Task](actions/get-crm-task.md) | GET |  |
| [List CRM Task Types](actions/list-crm-task-types.md) | GET |  |
| [List CRM Tasks](actions/list-crm-tasks.md) | GET |  |
| [Update CRM Task](actions/update-crm-task.md) | PUT |  |

### Transactional Email Log

| Action | Method | Description |
| --- | --- | --- |
| [List Transactional Emails](actions/list-transactional-emails.md) | GET |  |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Delete Object Records Batch](actions/delete-object-records-batch.md) | DELETE |  |
| [List Object Records](actions/list-object-records.md) | GET |  |
| [Upsert Object Records Batch](actions/upsert-object-records-batch.md) | POST |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create Corporate SSO Token](actions/create-corporate-sso-token.md) | POST |  |
| [Create Corporate Sub Account SSO Token](actions/create-corporate-sub-account-sso-token.md) | POST |  |
| [Get Corporate Invited User Permissions](actions/get-corporate-invited-user-permissions.md) | GET |  |
| [Get Corporate User Permissions](actions/get-corporate-user-permissions.md) | GET |  |
| [Get Organization User Permissions](actions/get-organization-user-permissions.md) | GET |  |
| [Invite Corporate Admin User](actions/invite-corporate-admin-user.md) | POST |  |
| [Invite Organization User](actions/invite-organization-user.md) | POST |  |
| [List Corporate Invited Users](actions/list-corporate-invited-users.md) | GET |  |
| [List Organization Activities](actions/list-organization-activities.md) | GET |  |
| [List Organization Invited Users](actions/list-organization-invited-users.md) | GET |  |
| [Revoke Corporate User](actions/revoke-corporate-user.md) | DELETE |  |
| [Revoke Organization User Permission](actions/revoke-organization-user-permission.md) | PUT |  |
| [Update Corporate User Invitation](actions/update-corporate-user-invitation.md) | PUT |  |
| [Update Corporate User Permissions](actions/update-corporate-user-permissions.md) | PUT |  |
| [Update Organization User Invitation](actions/update-organization-user-invitation.md) | PUT |  |
| [Update Organization User Permissions](actions/update-organization-user-permissions.md) | PUT |  |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST |  |
| [Delete Webhook](actions/delete-webhook.md) | DELETE |  |
| [Get Webhook](actions/get-webhook.md) | GET |  |
| [List Webhooks](actions/list-webhooks.md) | GET |  |
| [Update Webhook](actions/update-webhook.md) | PUT |  |

### Workflows

| Action | Method | Description |
| --- | --- | --- |
| [Get Process](actions/get-process.md) | GET |  |
| [List Processes](actions/list-processes.md) | GET |  |

