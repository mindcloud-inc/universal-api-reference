# <img src="https://images.mindcloud.co/apps/icons/geocodio_1776256301835.png" alt="Geocodio logo" width="28" height="28"> Geocodio: Universal API

Geocodio provides geocoding, reverse geocoding, data append, list geocoding, and distance APIs for addresses and coordinates in the United States, Canada, and Mexico.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/geocodio/latest
- **Category:** Support / Field Service
- **Actions:** 16
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.geocod.io/
- **Vendor API docs:** https://www.geocod.io/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Geocode Address](actions/geocode-address.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/geocode-address?connectionId=$CONNECTION_ID&q=1109%20N%20Highland%20St%2C%20Arlington%20VA" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (16)

### Address

| Action | Method | Description |
| --- | --- | --- |
| [Batch Geocode Addresses](actions/batch-geocode-addresses.md) | GET | Retrieves geocoding results from Geocodio for multiple addresses. |
| [Batch Reverse Geocode Coordinates](actions/batch-reverse-geocode-coordinates.md) | GET | Retrieves address details from Geocodio for multiple coordinates. |
| [Geocode Address](actions/geocode-address.md) | GET | Retrieves geocoding results from Geocodio for one address. |
| [Reverse Geocode Coordinate](actions/reverse-geocode-coordinate.md) | GET | Retrieves address details from Geocodio for one coordinate. |

### Distance

| Action | Method | Description |
| --- | --- | --- |
| [Calculate Distance From Origin](actions/calculate-distance-from-origin.md) | GET | Retrieves distances from one origin in Geocodio. |

### Distance Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Distance Job](actions/create-distance-job.md) | POST | Creates an asynchronous distance job in Geocodio. |
| [Delete Distance Job](actions/delete-distance-job.md) | DELETE | Deletes an asynchronous distance job from Geocodio. |
| [Get Distance Job](actions/get-distance-job.md) | GET | Retrieves an asynchronous distance job from Geocodio. |
| [List Distance Jobs](actions/list-distance-jobs.md) | GET | Retrieves asynchronous distance jobs from Geocodio. |

### Distance Job Results

| Action | Method | Description |
| --- | --- | --- |
| [Download Distance Job Results](actions/download-distance-job-results.md) | GET | Retrieves completed distance job results from Geocodio. |

### Distance Matrix

| Action | Method | Description |
| --- | --- | --- |
| [Calculate Distance Matrix](actions/calculate-distance-matrix.md) | GET | Retrieves a distance matrix from Geocodio. |

### Geocoding List

| Action | Method | Description |
| --- | --- | --- |
| [Create Geocoding List](actions/create-geocoding-list.md) | POST | Creates a new geocoding list in Geocodio. |
| [Delete Geocoding List](actions/delete-geocoding-list.md) | DELETE | Deletes an existing geocoding list from Geocodio. |
| [Get Geocoding List](actions/get-geocoding-list.md) | GET | Retrieves geocoding list status from Geocodio. |
| [List Geocoding Lists](actions/list-geocoding-lists.md) | GET | Retrieves geocoding lists from Geocodio. |

### Geocoding List Results

| Action | Method | Description |
| --- | --- | --- |
| [Download Geocoding List Results](actions/download-geocoding-list-results.md) | GET | Retrieves completed geocoding list results from Geocodio. |

