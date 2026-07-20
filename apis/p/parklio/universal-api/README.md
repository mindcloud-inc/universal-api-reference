# <img src="https://images.mindcloud.co/apps/icons/cropped-parklio-logo-1-32x32_1777051475451.png" alt="Parklio logo" width="28" height="28"> Parklio: Universal API

Manage parking lots, products, access, and occupancy data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/parklio/latest
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://parklio.com
- **Vendor API docs:** https://docs.parklio.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Products](actions/list-products.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/parklio/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Activities

| Action | Method | Description |
| --- | --- | --- |
| [List Key Logs](actions/list-key-logs.md) | GET | Retrieves key logs from Parklio. |

### Alerts

| Action | Method | Description |
| --- | --- | --- |
| [List Product Errors](actions/list-product-errors.md) | GET | Retrieves product errors from Parklio. |

### Devices

| Action | Method | Description |
| --- | --- | --- |
| [List Devices](actions/list-devices.md) | GET | Retrieves devices from Parklio. |
| [List Gates](actions/list-gates.md) | GET | Retrieves gates from Parklio. |
| [List Gateways](actions/list-gateways.md) | GET | Retrieves gateways from Parklio. |
| [List Terminals](actions/list-terminals.md) | GET | Retrieves terminals from Parklio. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [List Lot Entries](actions/list-lot-entries.md) | GET | Retrieves lot entries from Parklio. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [List Groups](actions/list-groups.md) | GET | Retrieves groups from Parklio. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Get Lot](actions/get-lot.md) | GET | Retrieves a lot from Parklio. |
| [Get Zone](actions/get-zone.md) | GET | Retrieves a zone from Parklio. |
| [List Lots](actions/list-lots.md) | GET | Retrieves lots from Parklio. |
| [List Parking Places](actions/list-parking-places.md) | GET | Retrieves parking places from Parklio. |
| [List Zones](actions/list-zones.md) | GET | Retrieves zones from Parklio. |
| [Update Lot Description](actions/update-lot-description.md) | PUT | Updates a lot description in Parklio. |
| [Update Zone Description](actions/update-zone-description.md) | PUT | Updates a zone description in Parklio. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [List Products](actions/list-products.md) | GET | Retrieves products from Parklio. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Product Counts](actions/get-account-product-counts.md) | GET | Retrieves account product counts from Parklio. |
| [List QR Codes](actions/list-qr-codes.md) | GET | Retrieves QR codes from Parklio. |
| [List Tariffs](actions/list-tariffs.md) | GET | Retrieves tariffs from Parklio. |
| [List Weblinks](actions/list-weblinks.md) | GET | Retrieves weblinks from Parklio. |

