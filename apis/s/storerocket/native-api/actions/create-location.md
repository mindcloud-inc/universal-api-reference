# Create Location with Storerocket

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId/locations`
- **Base URL:** `https://storerocket.io/api/v2`
- **Official documentation:** [Create Location](https://storerocket.io/api/v2/projects/:projectId/locations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The StoreRocket project ID that will receive the new location. |
| `name` | body | `string` | yes | Location display name. |
| `address_line_1` | body | `string` | yes | Primary street address for the location. |
| `address_line_2` | body | `string` | no | Secondary street address details. |
| `city` | body | `string` | yes | City for the location. |
| `postcode` | body | `string` | no | Postal code. |
| `country` | body | `string` | no | Country code or name. |
| `state` | body | `string` | no | State or region. |
| `phone` | body | `string` | no | Contact phone number. |
| `email` | body | `string` | no | Contact email address. |
| `url` | body | `string` | no | Public website URL for the location. |
| `facebook` | body | `string` | no | Facebook profile URL. |
| `instagram` | body | `string` | no | Instagram profile URL. |
| `twitter` | body | `string` | no | Twitter/X profile URL. |
| `yelp` | body | `string` | no | Yelp page URL. |
| `visible` | body | `boolean` | no | Whether the location is visible in the locator. |
| `lat` | body | `number` | no | Latitude override for the location. |
| `lng` | body | `number` | no | Longitude override for the location. |
