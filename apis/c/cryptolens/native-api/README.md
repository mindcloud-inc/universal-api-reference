# Cryptolens: Native API Reference

A consolidated summary of Cryptolens's API configuration and 55 documented operations, with links to official documentation.

- **Official docs:** https://app.cryptolens.io/docs/api/v3/
- **API base URL:** `https://api.cryptolens.io`

## Authentication

### Access Token

Cryptolens Web API access token sent as the required token query parameter on every request.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://app.cryptolens.io/docs/api/v3/Auth)

### Access Token Query Auth

Cryptolens Web API access token injected as the required token query parameter on every request.

### Credentials

- **Access Token:** `apiKey` · required · Cryptolens Web API access token.

[Official authentication documentation](https://app.cryptolens.io/docs/api/v3/Auth)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (55 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Activate](actions/activate.md) | `GET /api/key/Activate` | [docs](https://app.cryptolens.io/docs/api/v3/Activate) |
| [Add Customer](actions/add-customer.md) | `GET /api/customer/AddCustomer` | [docs](https://app.cryptolens.io/docs/api/v3/AddCustomer) |
| [Add Data Object](actions/add-data-object.md) | `GET /api/data/AddDataObject` | [docs](https://app.cryptolens.io/docs/api/v3/AddDataObject) |
| [Add Feature](actions/add-feature.md) | `GET /api/key/AddFeature` | [docs](https://app.cryptolens.io/docs/api/v3/AddFeature) |
| [Add Reseller](actions/add-reseller.md) | `GET /api/reseller/AddReseller` | [docs](https://app.cryptolens.io/docs/api/v3/AddReseller) |
| [Associate](actions/associate.md) | `GET /api/userauth/Associate` | [docs](https://app.cryptolens.io/docs/api/v3/Associate) |
| [Block Key](actions/block-key.md) | `GET /api/key/BlockKey` | [docs](https://app.cryptolens.io/docs/api/v3/BlockKey) |
| [Change Customer](actions/change-customer.md) | `GET /api/key/ChangeCustomer` | [docs](https://app.cryptolens.io/docs/api/v3/ChangeCustomer) |
| [Change Notes](actions/change-notes.md) | `GET /api/key/ChangeNotes` | [docs](https://app.cryptolens.io/docs/api/v3/ChangeNotes) |
| [Change Password](actions/change-password.md) | `GET /api/userauth/ChangePassword` | [docs](https://app.cryptolens.io/docs/api/v3/ChangePassword) |
| [Change Reseller](actions/change-reseller.md) | `GET /api/key/ChangeReseller` | [docs](https://app.cryptolens.io/docs/api/v3/ChangeReseller) |
| [Create Key](actions/create-key.md) | `GET /api/key/CreateKey` | [docs](https://app.cryptolens.io/docs/api/v3/CreateKey) |
| [Create Key From Template](actions/create-key-from-template.md) | `GET /api/key/CreateKeyFromTemplate` | [docs](https://app.cryptolens.io/docs/api/v3/CreateKeyFromTemplate) |
| [Create Message](actions/create-message.md) | `GET /api/message/CreateMessage` | [docs](https://app.cryptolens.io/docs/api/v3/CreateMessage) |
| [Create Session](actions/create-session.md) | `GET /api/paymentform/CreateSession` | [docs](https://app.cryptolens.io/docs/api/v3/PFCreateSession) |
| [Create Trial Key](actions/create-trial-key.md) | `GET /api/key/CreateTrialKey` | [docs](https://app.cryptolens.io/docs/api/v3/CreateTrialKey) |
| [Deactivate](actions/deactivate.md) | `GET /api/key/Deactivate` | [docs](https://app.cryptolens.io/docs/api/v3/Deactivate) |
| [Decrement Int Value](actions/decrement-int-value.md) | `GET /api/data/DecrementIntValue` | [docs](https://app.cryptolens.io/docs/api/v3/DecrementIntValue) |
| [Dissociate](actions/dissociate.md) | `GET /api/userauth/Dissociate` | [docs](https://app.cryptolens.io/docs/api/v3/Dissociate) |
| [Edit Customer](actions/edit-customer.md) | `GET /api/customer/EditCustomer` | [docs](https://app.cryptolens.io/docs/api/v3/EditCustomer) |
| [Edit Reseller](actions/edit-reseller.md) | `GET /api/reseller/EditReseller` | [docs](https://app.cryptolens.io/docs/api/v3/EditReseller) |
| [Extend License](actions/extend-license.md) | `GET /api/key/ExtendLicense` | [docs](https://app.cryptolens.io/docs/api/v3/ExtendLicense) |
| [Get Customer Licenses](actions/get-customer-licenses.md) | `GET /api/customer/GetCustomerLicenses` | [docs](https://app.cryptolens.io/docs/api/v3/GetCustomerLicenses) |
| [Get Customers](actions/get-customers.md) | `GET /api/customer/GetCustomers` | [docs](https://app.cryptolens.io/docs/api/v3/GetCustomers) |
| [Get Events](actions/get-events.md) | `GET /api/ai/GetEvents` | [docs](https://app.cryptolens.io/docs/api/v3/GetEvents) |
| [Get Key](actions/get-key.md) | `GET /api/key/GetKey` | [docs](https://app.cryptolens.io/docs/api/v3/GetKey) |
| [Get Keys](actions/get-keys.md) | `GET /api/product/GetKeys` | [docs](https://app.cryptolens.io/docs/api/v3/GetKeys) |
| [Get License Templates](actions/get-license-templates.md) | `GET /api/licensetemplate/GetLicenseTemplates` | [docs](https://app.cryptolens.io/docs/api/v3/GetLicenseTemplates) |
| [Get Messages](actions/get-messages.md) | `GET /api/message/GetMessages` | [docs](https://app.cryptolens.io/docs/api/v3/GetMessages) |
| [Get Object Log](actions/get-object-log.md) | `GET /api/ai/GetObjectLog` | [docs](https://app.cryptolens.io/docs/api/v3/GetObjectLog) |
| [Get Reseller Customers](actions/get-reseller-customers.md) | `GET /api/reseller/GetResellerCustomers` | [docs](https://app.cryptolens.io/docs/api/v3/GetResellerCustomers) |
| [Get Resellers](actions/get-resellers.md) | `GET /api/reseller/GetResellers` | [docs](https://app.cryptolens.io/docs/api/v3/GetResellers) |
| [Get Users](actions/get-users.md) | `GET /api/userauth/GetUsers` | [docs](https://app.cryptolens.io/docs/api/v3/GetUsers) |
| [Get Web API Log](actions/get-web-api-log.md) | `GET /api/ai/GetWebAPILog` | [docs](https://app.cryptolens.io/docs/api/v3/GetWebAPILog) |
| [Increment Int Value](actions/increment-int-value.md) | `GET /api/data/IncrementIntValue` | [docs](https://app.cryptolens.io/docs/api/v3/IncrementIntValue) |
| [Key Lock](actions/key-lock.md) | `GET /api/auth/KeyLock` | [docs](https://app.cryptolens.io/docs/api/v3/KeyLock) |
| [List Data Objects](actions/list-data-objects.md) | `GET /api/data/ListDataObjects` | [docs](https://app.cryptolens.io/docs/api/v3/ListDataObjects) |
| [List Products](actions/list-products.md) | `GET /api/product/GetProducts` | [docs](https://app.cryptolens.io/docs/api/v3/GetProducts) |
| [Login](actions/login.md) | `GET /api/userauth/Login` | [docs](https://app.cryptolens.io/docs/api/v3/Login) |
| [Machine Lock Limit](actions/machine-lock-limit.md) | `GET /api/key/MachineLockLimit` | [docs](https://app.cryptolens.io/docs/api/v3/MachineLockLimit) |
| [Record Usage](actions/record-usage.md) | `GET /api/subscription/RecordUsage` | [docs](https://app.cryptolens.io/docs/api/v3/RecordUsage) |
| [Register](actions/register.md) | `GET /api/userauth/Register` | [docs](https://app.cryptolens.io/docs/api/v3/Register) |
| [Register Event](actions/register-event.md) | `GET /api/ai/RegisterEvent` | [docs](https://app.cryptolens.io/docs/api/v3/RegisterEvent) |
| [Remove Customer](actions/remove-customer.md) | `GET /api/customer/RemoveCustomer` | [docs](https://app.cryptolens.io/docs/api/v3/RemoveCustomer) |
| [Remove Data Object](actions/remove-data-object.md) | `GET /api/data/RemoveDataObject` | [docs](https://app.cryptolens.io/docs/api/v3/RemoveDataObject) |
| [Remove Feature](actions/remove-feature.md) | `GET /api/key/RemoveFeature` | [docs](https://app.cryptolens.io/docs/api/v3/RemoveFeature) |
| [Remove Message](actions/remove-message.md) | `GET /api/message/RemoveMessage` | [docs](https://app.cryptolens.io/docs/api/v3/RemoveMessage) |
| [Remove Reseller](actions/remove-reseller.md) | `GET /api/reseller/RemoveReseller` | [docs](https://app.cryptolens.io/docs/api/v3/RemoveReseller) |
| [Remove User](actions/remove-user.md) | `GET /api/userauth/RemoveUser` | [docs](https://app.cryptolens.io/docs/api/v3/RemoveUser) |
| [Reset Password Token](actions/reset-password-token.md) | `GET /api/userauth/ResetPasswordToken` | [docs](https://app.cryptolens.io/docs/api/v3/ResetPasswordToken) |
| [Set Int Value](actions/set-int-value.md) | `GET /api/data/SetIntValue` | [docs](https://app.cryptolens.io/docs/api/v3/SetIntValue) |
| [Set String Value](actions/set-string-value.md) | `GET /api/data/SetStringValue` | [docs](https://app.cryptolens.io/docs/api/v3/SetStringValue) |
| [Trial Activation](actions/trial-activation.md) | `GET /api/key/TrialActivation` | [docs](https://app.cryptolens.io/docs/api/v3/TrialActivation) |
| [Unblock Key](actions/unblock-key.md) | `GET /api/key/UnblockKey` | [docs](https://app.cryptolens.io/docs/api/v3/UnblockKey) |
| [Upload Values](actions/upload-values.md) | `GET /api/data/UploadValuesToKey` | [docs](https://app.cryptolens.io/docs/api/v3/UploadValues) |
