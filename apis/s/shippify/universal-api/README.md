# <img src="https://images.mindcloud.co/apps/icons/favicon-32x32_1775817882065.png" alt="Shippify logo" width="28" height="28"> Shippify: Universal API

Plan, route, and manage delivery operations with the Shippify API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/shippify/latest
- **Category:** Commerce / Supply Chain
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://shippify.co/
- **Vendor API docs:** https://docs.shippify.co/developers/en/shippify-api/first-steps

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Countries](actions/list-countries.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shippify/latest/actions/list-countries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Country

| Action | Method | Description |
| --- | --- | --- |
| [List Countries](actions/list-countries.md) | GET | Retrieves the list of supported countries from Shippify. |

### Delivery

| Action | Method | Description |
| --- | --- | --- |
| [Change Delivery Status](actions/change-delivery-status.md) | PUT | Updates a delivery status in Shippify. |
| [Create Deliveries](actions/create-deliveries.md) | POST | Creates up to 100 deliveries in Shippify. |
| [Get Delivery Information](actions/get-delivery-information.md) | GET | Retrieves delivery details from Shippify by ID or reference. |
| [Update Delivery](actions/update-delivery.md) | PUT | Updates delivery details in Shippify by ID or reference. |
| [Update Pickup Point](actions/update-pickup-point.md) | PUT | Updates pickup details for deliveries in Shippify. |

### Delivery Label

| Action | Method | Description |
| --- | --- | --- |
| [Print Delivery Labels](actions/print-delivery-labels.md) | GET | Retrieves PDF delivery labels from Shippify. |

### Delivery Quote

| Action | Method | Description |
| --- | --- | --- |
| [Get Delivery Quotes](actions/get-delivery-quotes.md) | GET | Retrieves delivery quotes from Shippify for up to 100 deliveries. |

### Route

| Action | Method | Description |
| --- | --- | --- |
| [Add Deliveries To Route](actions/add-deliveries-to-route.md) | PUT | Adds deliveries to an existing route in Shippify. |
| [Break Route](actions/break-route.md) | DELETE | Deletes routes in Shippify and returns deliveries to processing. |
| [Change Route Status](actions/change-route-status.md) | PUT | Updates a route status in Shippify. |
| [Create Route](actions/create-route.md) | POST | Creates delivery routes in Shippify asynchronously. |
| [Get Route Information](actions/get-route-information.md) | GET | Retrieves route details from Shippify by route or delivery ID. |
| [Remove Deliveries From Route](actions/remove-deliveries-from-route.md) | PUT | Removes deliveries from an existing route in Shippify. |

### Tracking Link

| Action | Method | Description |
| --- | --- | --- |
| [Get Tracking Link](actions/get-tracking-link.md) | GET | Retrieves a secure delivery tracking link from Shippify. |

