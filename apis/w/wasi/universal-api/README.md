# <img src="https://images.mindcloud.co/apps/icons/wasi_1774461885688.png" alt="Wasi logo" width="28" height="28"> Wasi: Universal API

Wasi is a real estate CRM and property management platform for brokers and agencies to manage properties, clients, and real estate operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/wasi/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://wasi.co
- **Vendor API docs:** https://api.wasi.co/docs/en/guide/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Properties](actions/list-properties.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wasi/latest/actions/list-properties?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### City

| Action | Method | Description |
| --- | --- | --- |
| [List Cities With Property](actions/list-cities-with-property.md) | GET | Retrieves cities with assigned properties from Wasi. |

### Client

| Action | Method | Description |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | POST | Creates a new client in Wasi. |
| [Get Client](actions/get-client.md) | GET | Retrieves a client from Wasi. |
| [List Clients](actions/list-clients.md) | GET | Finds clients in Wasi by search criteria. |
| [List Property Clients](actions/list-property-clients.md) | GET | Retrieves clients linked to a property in Wasi. |
| [Update Client](actions/update-client.md) | PUT | Updates an existing client in Wasi. |

### Client Property Link

| Action | Method | Description |
| --- | --- | --- |
| [Link Client To Property](actions/link-client-to-property.md) | POST | Creates a client-to-property relationship in Wasi. |
| [Remove Client Property Link](actions/remove-client-property-link.md) | DELETE | Deletes a client-to-property relationship from Wasi. |
| [Update Client Property Link](actions/update-client-property-link.md) | PUT | Updates a client-to-property relationship in Wasi. |

### Client Type

| Action | Method | Description |
| --- | --- | --- |
| [List Client Types](actions/list-client-types.md) | GET | Retrieves client types from Wasi. |

### Country

| Action | Method | Description |
| --- | --- | --- |
| [List Countries](actions/list-countries.md) | GET | Retrieves countries from Wasi. |

### Currency

| Action | Method | Description |
| --- | --- | --- |
| [List Currencies](actions/list-currencies.md) | GET | Retrieves currencies from Wasi. |

### Property

| Action | Method | Description |
| --- | --- | --- |
| [Change Property Label](actions/change-property-label.md) | PUT | Updates a property label in Wasi. |
| [Create Property](actions/create-property.md) | POST | Creates a new property in Wasi. |
| [Get Property](actions/get-property.md) | GET | Retrieves a property from Wasi. |
| [Get Property Commission](actions/get-property-commission.md) | GET | Retrieves a property's commission details from Wasi. |
| [List Client Properties](actions/list-client-properties.md) | GET | Retrieves properties linked to a client in Wasi. |
| [List Properties](actions/list-properties.md) | GET | Finds properties in Wasi by search criteria. |
| [Remove Property Label](actions/remove-property-label.md) | PUT | Removes a property label from Wasi. |
| [Send Property To Portals](actions/send-property-to-portals.md) | PUT | Updates a property's portal sync in Wasi. |
| [Update Property](actions/update-property.md) | PUT | Updates an existing property in Wasi. |

### Property Image

| Action | Method | Description |
| --- | --- | --- |
| [Remove Property Image](actions/remove-property-image.md) | DELETE | Deletes a property image from Wasi. |
| [Update Property Image](actions/update-property-image.md) | PUT | Updates a property image in Wasi. |
| [Upload Property Image](actions/upload-property-image.md) | POST | Uploads a property image to Wasi. |

### Property Type

| Action | Method | Description |
| --- | --- | --- |
| [List Property Types](actions/list-property-types.md) | GET | Retrieves property types from Wasi. |

