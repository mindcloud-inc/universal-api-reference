# GraphHopper: Native API Reference

A consolidated summary of GraphHopper's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://docs.graphhopper.com/openapi/
- **OpenAPI specification:** https://docs.graphhopper.com/_bundle/openapi.json?download=
- **API base URL:** `https://graphhopper.com/api/1`

## Authentication

### API Key

Authenticate with a GraphHopper API key sent as the shared `key` query parameter on every request.

### Credentials

- **API Key:** `apiKey` · required · Your GraphHopper API key.

[Official authentication documentation](https://support.graphhopper.com/a/solutions/articles/44001976027)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Calculate Route](actions/calculate-route.md) | `POST /route` | [docs](https://docs.graphhopper.com/openapi/routing/postroute) |
| [Compute Isochrone](actions/compute-isochrone.md) | `GET /isochrone` | [docs](https://docs.graphhopper.com/openapi/isochrones/getisochrone) |
| [Compute Matrix](actions/compute-matrix.md) | `POST /matrix` | [docs](https://docs.graphhopper.com/openapi/matrices/postmatrix) |
| [Create Custom Routing Profile](actions/create-custom-routing-profile.md) | `POST /profiles` | [docs](https://docs.graphhopper.com/openapi/custom-profiles/postprofiles) |
| [Delete Custom Routing Profile](actions/delete-custom-routing-profile.md) | `DELETE /profiles/:profileId` | [docs](https://docs.graphhopper.com/openapi/custom-profiles/deleteprofilesprofileid) |
| [Get Clustering Solution](actions/get-clustering-solution.md) | `GET /cluster/solution/:jobId` | [docs](https://docs.graphhopper.com/openapi/clustering/getclustersolutionjobid) |
| [Get Custom Profile Creation Result](actions/get-custom-profile-creation-result.md) | `GET /profiles/solution/:jobId` | [docs](https://docs.graphhopper.com/openapi/custom-profiles/getprofilessolutionjobid) |
| [Geocode Location](actions/get-geocode.md) | `GET /geocode` | [docs](https://docs.graphhopper.com/openapi/geocoding/getgeocode) |
| [Get Matrix Job Result](actions/get-matrix-job-result.md) | `GET /matrix/solution/:jobId` | [docs](https://docs.graphhopper.com/openapi/matrices/getmatrixsolutionjobid) |
| [Get Route Optimization Solution](actions/get-route-optimization-solution.md) | `GET /vrp/solution/:jobId` | [docs](https://docs.graphhopper.com/openapi/route-optimization/getvrpsolutionjobid) |
| [List Custom Routing Profiles](actions/list-custom-routing-profiles.md) | `GET /profiles` | [docs](https://docs.graphhopper.com/openapi/custom-profiles/getprofiles) |
| [Match GPX Trace](actions/match-gpx-trace.md) | `POST /match` | [docs](https://docs.graphhopper.com/openapi/map-matching/postmatch) |
| [Solve Clustering Problem](actions/solve-clustering-problem.md) | `POST /cluster` | [docs](https://docs.graphhopper.com/openapi/clustering/postcluster) |
| [Solve Route Optimization Problem](actions/solve-route-optimization-problem.md) | `POST /vrp` | [docs](https://docs.graphhopper.com/openapi/route-optimization/postvrp) |
| [Submit Clustering Job](actions/submit-clustering-job.md) | `POST /cluster/calculate` | [docs](https://docs.graphhopper.com/openapi/clustering/postclustercalculate) |
| [Submit Custom Profile Creation Job](actions/submit-custom-profile-creation-job.md) | `POST /profiles/calculate` | [docs](https://docs.graphhopper.com/openapi/custom-profiles/postprofilescalculate) |
| [Submit Matrix Job](actions/submit-matrix-job.md) | `POST /matrix/calculate` | [docs](https://docs.graphhopper.com/openapi/matrices/postmatrixcalculate) |
| [Submit Route Optimization Job](actions/submit-route-optimization-job.md) | `POST /vrp/optimize` | [docs](https://docs.graphhopper.com/openapi/route-optimization/postvrpoptimize) |
