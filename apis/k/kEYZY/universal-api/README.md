# <img src="https://images.mindcloud.co/apps/icons/k-eyzy_1775575269548.png" alt="KEYZY logo" width="28" height="28"> KEYZY: Universal API

Manage software licenses, activations, and product access

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/kEYZY/latest
- **Category:** Commerce
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://app.keyzy.io
- **Vendor API docs:** https://www.keyzy.io/docs/developers/rest-api/general-requirements/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Status Check](actions/get-status-check.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kEYZY/latest/actions/get-status-check?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Activation

| Action | Method | Description |
| --- | --- | --- |
| [Delete Activation](actions/delete-activation.md) | DELETE | Deletes a license activation from KEYZY. |
| [List Activations](actions/list-activations.md) | GET | Retrieves activations for a KEYZY license serial number. |
| [Update Activation](actions/update-activation.md) | PUT | Updates a license activation in KEYZY. |

### License

| Action | Method | Description |
| --- | --- | --- |
| [Get License](actions/get-license.md) | GET | Retrieves details for a specific KEYZY license. |
| [Register License](actions/register-license.md) | POST | Registers a new customer to a KEYZY license. |
| [Update License SKU](actions/update-license-sku.md) | PUT | Updates the connected SKU for a KEYZY license. |
| [Update License Time](actions/update-license-time.md) | PUT | Updates start and end times for a KEYZY license. |
| [Upgrade License](actions/upgrade-license.md) | PUT | Upgrades a KEYZY license from another license. |
| [Validate License](actions/validate-license.md) | GET | Validates a software license in KEYZY. |

### License File

| Action | Method | Description |
| --- | --- | --- |
| [Get Encrypted License File](actions/get-encrypted-license-file.md) | GET | Validates a KEYZY license and retrieves an encrypted license file. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [List License Products](actions/list-license-products.md) | GET | Retrieves products related to a KEYZY license. |

### Registered Product

| Action | Method | Description |
| --- | --- | --- |
| [List Register Products](actions/list-register-products.md) | GET | Checks serial eligibility and previews registered products in KEYZY. |
| [Update Register Products](actions/update-register-products.md) | PUT | Registers a KEYZY product to a licensee. |

### Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Status Check](actions/get-status-check.md) | GET | Retrieves the current API server status from KEYZY. |

