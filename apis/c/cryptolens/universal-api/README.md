# <img src="https://images.mindcloud.co/apps/icons/cryptolens_1774558470520.png" alt="Cryptolens logo" width="28" height="28"> Cryptolens: Universal API

Use the Devolens/Cryptolens Web API 3 to manage software licensing products, license keys, customers, users, resellers, messages, data objects, subscriptions, analytics, and license templates.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cryptolens/latest
- **Actions:** 55
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://devolens.com
- **Vendor API docs:** https://app.cryptolens.io/docs/api/v3/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Products](actions/list-products.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/list-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (55)

### Auth

| Action | Method | Description |
| --- | --- | --- |
| [Key Lock](actions/key-lock.md) | PUT | Locks an access token to a license key in Cryptolens. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Add Customer](actions/add-customer.md) | POST | Creates a new customer in Cryptolens. |
| [Edit Customer](actions/edit-customer.md) | PUT | Updates an existing customer in Cryptolens. |
| [Get Customer Licenses](actions/get-customer-licenses.md) | GET | Retrieves license keys for a customer from Cryptolens. |
| [Get Customers](actions/get-customers.md) | GET | Retrieves customers from Cryptolens. |
| [Remove Customer](actions/remove-customer.md) | DELETE | Deletes an existing customer from Cryptolens. |

### Data Object

| Action | Method | Description |
| --- | --- | --- |
| [Add Data Object](actions/add-data-object.md) | POST | Creates a new data object in Cryptolens. |
| [Decrement Int Value](actions/decrement-int-value.md) | PUT | Decrements a data object integer value in Cryptolens. |
| [Increment Int Value](actions/increment-int-value.md) | PUT | Increments a data object integer value in Cryptolens. |
| [List Data Objects](actions/list-data-objects.md) | GET | Retrieves data objects from Cryptolens. |
| [Remove Data Object](actions/remove-data-object.md) | DELETE | Deletes an existing data object from Cryptolens. |
| [Set Int Value](actions/set-int-value.md) | PUT | Updates a data object integer value in Cryptolens. |
| [Set String Value](actions/set-string-value.md) | PUT | Updates a data object string value in Cryptolens. |
| [Upload Values](actions/upload-values.md) | PUT | Uploads log values to data objects in Cryptolens. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Events](actions/get-events.md) | GET | Retrieves analytics events from Cryptolens. |
| [Register Event](actions/register-event.md) | POST | Creates an analytics event in Cryptolens. |

### License Key

| Action | Method | Description |
| --- | --- | --- |
| [Activate](actions/activate.md) | PUT | Activates a license key in Cryptolens. |
| [Add Feature](actions/add-feature.md) | POST | Adds a feature to a license key in Cryptolens. |
| [Block Key](actions/block-key.md) | PUT | Blocks a license key in Cryptolens. |
| [Change Customer](actions/change-customer.md) | PUT | Updates the customer on a license in Cryptolens. |
| [Change Notes](actions/change-notes.md) | PUT | Updates notes on a license key in Cryptolens. |
| [Change Reseller](actions/change-reseller.md) | PUT | Updates the reseller on a license in Cryptolens. |
| [Create Key](actions/create-key.md) | POST | Creates a new license key in Cryptolens. |
| [Create Key From Template](actions/create-key-from-template.md) | POST | Creates a license key from a template in Cryptolens. |
| [Create Trial Key](actions/create-trial-key.md) | POST | Creates a new trial key in Cryptolens. |
| [Deactivate](actions/deactivate.md) | PUT | Deactivates a license key in Cryptolens. |
| [Extend License](actions/extend-license.md) | PUT | Extends a license in Cryptolens. |
| [Get Key](actions/get-key.md) | GET | Retrieves a license key from Cryptolens. |
| [Get Keys](actions/get-keys.md) | GET | Retrieves license keys for a product from Cryptolens. |
| [Machine Lock Limit](actions/machine-lock-limit.md) | PUT | Updates a license key machine lock limit in Cryptolens. |
| [Remove Feature](actions/remove-feature.md) | DELETE | Deletes a feature from a license key in Cryptolens. |
| [Trial Activation](actions/trial-activation.md) | PUT | Enables trial activation on a license in Cryptolens. |
| [Unblock Key](actions/unblock-key.md) | PUT | Unblocks a license key in Cryptolens. |

### License Template

| Action | Method | Description |
| --- | --- | --- |
| [Get License Templates](actions/get-license-templates.md) | GET | Retrieves license templates from Cryptolens. |

### Message

| Action | Method | Description |
| --- | --- | --- |
| [Create Message](actions/create-message.md) | POST | Creates a new message in Cryptolens. |
| [Get Messages](actions/get-messages.md) | GET | Retrieves messages from Cryptolens. |
| [Remove Message](actions/remove-message.md) | DELETE | Deletes an existing message from Cryptolens. |

### Object Log

| Action | Method | Description |
| --- | --- | --- |
| [Get Object Log](actions/get-object-log.md) | GET | Retrieves object logs from Cryptolens. |

### Payment Session

| Action | Method | Description |
| --- | --- | --- |
| [Create Session](actions/create-session.md) | POST | Creates a payment form session in Cryptolens. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [List Products](actions/list-products.md) | GET | Retrieves products from Cryptolens. |

### Reseller

| Action | Method | Description |
| --- | --- | --- |
| [Add Reseller](actions/add-reseller.md) | POST | Creates a new reseller in Cryptolens. |
| [Edit Reseller](actions/edit-reseller.md) | PUT | Updates an existing reseller in Cryptolens. |
| [Get Reseller Customers](actions/get-reseller-customers.md) | GET | Retrieves customers for a reseller from Cryptolens. |
| [Get Resellers](actions/get-resellers.md) | GET | Retrieves resellers from Cryptolens. |
| [Remove Reseller](actions/remove-reseller.md) | DELETE | Deletes an existing reseller from Cryptolens. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Record Usage](actions/record-usage.md) | PUT | Records subscription usage in Cryptolens. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Associate](actions/associate.md) | PUT | Associates a user with a customer in Cryptolens. |
| [Change Password](actions/change-password.md) | PUT | Updates a user password in Cryptolens. |
| [Dissociate](actions/dissociate.md) | PUT | Dissociates a user from a customer in Cryptolens. |
| [Get Users](actions/get-users.md) | GET | Retrieves users from Cryptolens. |
| [Login](actions/login.md) | POST | Logs a user in to Cryptolens. |
| [Register](actions/register.md) | POST | Creates a new user in Cryptolens. |
| [Remove User](actions/remove-user.md) | DELETE | Deletes an existing user from Cryptolens. |
| [Reset Password Token](actions/reset-password-token.md) | POST | Creates a password reset token in Cryptolens. |

### Web Api Log

| Action | Method | Description |
| --- | --- | --- |
| [Get Web API Log](actions/get-web-api-log.md) | GET | Retrieves Web API logs from Cryptolens. |

