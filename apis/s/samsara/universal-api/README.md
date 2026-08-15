# <img src="https://files.readme.io/e946b5a-favicon.ico" alt="Samsara logo" width="28" height="28"> Samsara: Universal API

Connect Samsara fleet, driver, vehicle, asset, routing, safety, and compliance data to MindCloud workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/samsara/latest
- **Actions:** 26
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.samsara.com/
- **Vendor API docs:** https://developers.samsara.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Organization](actions/get-organization.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/samsara/latest/actions/get-organization?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (26)

### Address

| Action | Method | Description |
| --- | --- | --- |
| [Get Address](actions/get-address.md) | GET |  |
| [List Addresses](actions/list-addresses.md) | GET |  |

### Asset

| Action | Method | Description |
| --- | --- | --- |
| [List Assets](actions/list-assets.md) | GET |  |

### Driver

| Action | Method | Description |
| --- | --- | --- |
| [Get Driver](actions/get-driver.md) | GET |  |
| [List Drivers](actions/list-all-drivers.md) | GET |  |

### Driver-vehicle Assignment

| Action | Method | Description |
| --- | --- | --- |
| [List Driver-Vehicle Assignments](actions/list-driver-vehicle-assignments.md) | GET |  |

### Dvir

| Action | Method | Description |
| --- | --- | --- |
| [Stream DVIRs](actions/stream-dvirs.md) | GET |  |

### Dvir Defect

| Action | Method | Description |
| --- | --- | --- |
| [Stream DVIR Defects](actions/stream-dvir-defects.md) | GET |  |

### Equipment

| Action | Method | Description |
| --- | --- | --- |
| [Get Equipment](actions/get-equipment.md) | GET |  |
| [List Equipment](actions/list-equipment.md) | GET |  |

### Hos Clock

| Action | Method | Description |
| --- | --- | --- |
| [Get HOS Clocks](actions/get-hos-clocks.md) | GET |  |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET |  |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Create Driver](actions/create-driver.md) | POST |  |
| [Update Driver](actions/update-driver.md) | PATCH |  |

### Route

| Action | Method | Description |
| --- | --- | --- |
| [List Routes](actions/list-routes.md) | GET |  |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Get Tag](actions/get-tag.md) | GET |  |
| [List Tags](actions/list-all-tags1.md) | GET |  |

### Trailer

| Action | Method | Description |
| --- | --- | --- |
| [Get Trailer](actions/get-trailer.md) | GET |  |
| [List Trailers](actions/list-trailers.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET |  |
| [List Users](actions/list-users.md) | GET |  |

### User Role

| Action | Method | Description |
| --- | --- | --- |
| [List User Roles](actions/list-user-roles.md) | GET |  |

### Vehicle

| Action | Method | Description |
| --- | --- | --- |
| [Get Vehicle](actions/get-vehicle.md) | GET |  |
| [List Vehicles](actions/list-all-vehicles.md) | GET |  |

### Vehicle Location

| Action | Method | Description |
| --- | --- | --- |
| [Get Vehicle Locations](actions/get-vehicle-locations.md) | GET |  |

### Vehicle Stat

| Action | Method | Description |
| --- | --- | --- |
| [Get Vehicle Stats](actions/get-vehicle-stats.md) | GET |  |

