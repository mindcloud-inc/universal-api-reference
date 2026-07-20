# <img src="https://images.mindcloud.co/apps/icons/graph-hopper_1776265904633.png" alt="GraphHopper logo" width="28" height="28"> GraphHopper: Universal API

Routing, geocoding, map matching, matrix, isochrone, route optimization, clustering, and custom profile APIs from GraphHopper.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/graphHopper/latest
- **Category:** Commerce / Supply Chain
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.graphhopper.com/
- **Vendor API docs:** https://docs.graphhopper.com/openapi/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Geocode Location](actions/get-geocode.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/graphHopper/latest/actions/get-geocode?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Cluster Solution

| Action | Method | Description |
| --- | --- | --- |
| [Solve Clustering Problem](actions/solve-clustering-problem.md) | GET | Solves a clustering problem in GraphHopper. |

### Clustering Job

| Action | Method | Description |
| --- | --- | --- |
| [Submit Clustering Job](actions/submit-clustering-job.md) | POST | Submits a clustering job in GraphHopper. |

### Clustering Solution

| Action | Method | Description |
| --- | --- | --- |
| [Get Clustering Solution](actions/get-clustering-solution.md) | GET | Retrieves a clustering solution from GraphHopper. |

### Custom Profile Job

| Action | Method | Description |
| --- | --- | --- |
| [Submit Custom Profile Creation Job](actions/submit-custom-profile-creation-job.md) | POST | Submits a custom profile creation job in GraphHopper. |

### Custom Profile Job Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Custom Profile Creation Result](actions/get-custom-profile-creation-result.md) | GET | Retrieves a custom profile creation result from GraphHopper. |

### Custom Routing Profile

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Routing Profile](actions/create-custom-routing-profile.md) | POST | Creates a custom routing profile in GraphHopper. |
| [Delete Custom Routing Profile](actions/delete-custom-routing-profile.md) | DELETE | Deletes a custom routing profile from GraphHopper. |
| [List Custom Routing Profiles](actions/list-custom-routing-profiles.md) | GET | Retrieves custom routing profiles from GraphHopper. |

### Geocode Result

| Action | Method | Description |
| --- | --- | --- |
| [Geocode Location](actions/get-geocode.md) | GET | Retrieves geocoding results for a query in GraphHopper. |

### Isochrone

| Action | Method | Description |
| --- | --- | --- |
| [Compute Isochrone](actions/compute-isochrone.md) | GET | Computes an isochrone map in GraphHopper. |

### Matched Route

| Action | Method | Description |
| --- | --- | --- |
| [Match GPX Trace](actions/match-gpx-trace.md) | GET | Matches a GPX trace in GraphHopper. |

### Matrix

| Action | Method | Description |
| --- | --- | --- |
| [Compute Matrix](actions/compute-matrix.md) | GET | Computes a route matrix in GraphHopper. |

### Matrix Job

| Action | Method | Description |
| --- | --- | --- |
| [Submit Matrix Job](actions/submit-matrix-job.md) | POST | Submits a matrix job in GraphHopper. |

### Matrix Job Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Matrix Job Result](actions/get-matrix-job-result.md) | GET | Retrieves a matrix job result from GraphHopper. |

### Route

| Action | Method | Description |
| --- | --- | --- |
| [Calculate Route](actions/calculate-route.md) | GET | Calculates a route between points in GraphHopper. |

### Route Optimization

| Action | Method | Description |
| --- | --- | --- |
| [Solve Route Optimization Problem](actions/solve-route-optimization-problem.md) | GET | Solves a route optimization problem in GraphHopper. |

### Route Optimization Job

| Action | Method | Description |
| --- | --- | --- |
| [Submit Route Optimization Job](actions/submit-route-optimization-job.md) | POST | Submits a route optimization job in GraphHopper. |

### Route Optimization Solution

| Action | Method | Description |
| --- | --- | --- |
| [Get Route Optimization Solution](actions/get-route-optimization-solution.md) | GET | Retrieves a route optimization solution from GraphHopper. |

