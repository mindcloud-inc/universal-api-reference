# <img src="https://images.mindcloud.co/apps/icons/images_1782734349151.png" alt="Shippo - Legacy logo" width="28" height="28"> Shippo - Legacy: Universal API

Multi-carrier shipping and label API for addresses, parcels, shipments, labels, tracking, refunds, orders, and carrier accounts.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/shippo/latest
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://goshippo.com/
- **Vendor API docs:** https://docs.goshippo.com/shippoapi/public-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Carrier Accounts](actions/list-carrier-accounts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shippo/latest/actions/list-carrier-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Address

| Action | Method | Description |
| --- | --- | --- |
| [List Addresses](actions/list-addresses.md) | GET | Retrieves saved shipping addresses from Shippo. |

### Carrier Parcel Templates

| Action | Method | Description |
| --- | --- | --- |
| [List All Carrier Parcel Templates](actions/list-all-carrier-parcel-templates.md) | GET | Retrieves carrier parcel templates from Shippo. |

### Label

| Action | Method | Description |
| --- | --- | --- |
| [Create Insta Label](actions/create-insta-label.md) | POST | Creates a shipping label in one Shippo API call. |
| [Create Label with Rate ID](actions/create-label-with-rate-id.md) | POST | Creates a shipping label in Shippo from a rate ID. |
| [List Transactions](actions/list-transactions.md) | GET | Retrieves existing shipping labels from Shippo. |

### Refund

| Action | Method | Description |
| --- | --- | --- |
| [Create Refund](actions/create-refund.md) | POST | Creates a refund for a Shippo shipping label. |

### Shipment

| Action | Method | Description |
| --- | --- | --- |
| [Create Shipment](actions/create-shipment.md) | POST | Creates a new shipment in Shippo. |

### Shipping Carrier

| Action | Method | Description |
| --- | --- | --- |
| [List Carrier Accounts](actions/list-carrier-accounts.md) | GET | Retrieves carrier accounts connected to your Shippo account. |

