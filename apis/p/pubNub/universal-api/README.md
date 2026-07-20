# <img src="https://images.mindcloud.co/apps/icons/id-nk-xhv-gx-k-1775858238067_1775858243513.jpeg" alt="PubNub logo" width="28" height="28"> PubNub: Universal API

PubNub is a real-time messaging and event-streaming platform for building chat, live collaboration, alerts, and multi-tenant communication systems.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pubNub/latest
- **Category:** Communication / Team Messaging
- **Actions:** 34
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.pubnub.com
- **Vendor API docs:** https://www.pubnub.com/docs/admin-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Usage Metrics](actions/get-usage-metrics.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pubNub/latest/actions/get-usage-metrics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (34)

### App

| Action | Method | Description |
| --- | --- | --- |
| [Create App](actions/create-app.md) | POST | Creates an app in PubNub. |
| [Delete App](actions/delete-app.md) | DELETE | Deletes an existing app from PubNub. |
| [Get App](actions/get-app.md) | GET | Retrieves an app from PubNub. |
| [List Apps](actions/list-apps.md) | GET | Retrieves apps from PubNub. |
| [Update App](actions/update-app.md) | PUT | Updates an existing app in PubNub. |

### Applications

| Action | Method | Description |
| --- | --- | --- |
| [List Applications For Customer](actions/list-applications-for-customer.md) | GET | Retrieves applications for a PubNub customer. |

### Business Units

| Action | Method | Description |
| --- | --- | --- |
| [List Business Objects](actions/list-business-objects.md) | GET | Retrieves business objects from PubNub Illuminate. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Assign Keysets To Customer](actions/assign-keysets-to-customer.md) | PUT | Assigns keysets to a PubNub customer. |
| [Create Customer](actions/create-customer.md) | POST | Creates a customer in PubNub. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from PubNub. |
| [Get Customer By Keyset](actions/get-customer-by-keyset.md) | GET | Retrieves a PubNub customer by keyset. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from PubNub. |
| [List Keysets For Customer](actions/list-keysets-for-customer.md) | GET | Retrieves keysets for a PubNub customer. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in PubNub. |

### Dashboards

| Action | Method | Description |
| --- | --- | --- |
| [List Dashboards](actions/list-dashboards.md) | GET | Retrieves dashboards from PubNub Illuminate. |

### Data Sources

| Action | Method | Description |
| --- | --- | --- |
| [Get Insights Data](actions/get-insights-data.md) | GET | Retrieves insights data from PubNub. |
| [Get Top N Insights Data](actions/get-top-n-insights-data.md) | GET | Retrieves top N insights data from PubNub. |

### Decision

| Action | Method | Description |
| --- | --- | --- |
| [List Decisions](actions/list-decisions.md) | GET | Retrieves decisions from PubNub Illuminate. |

### Keyset

| Action | Method | Description |
| --- | --- | --- |
| [Create Keyset](actions/create-keyset.md) | POST | Creates a keyset in PubNub. |
| [Delete Keyset](actions/delete-keyset.md) | DELETE | Deletes an existing keyset from PubNub. |
| [Get Keyset](actions/get-keyset.md) | GET | Retrieves a keyset from PubNub. |
| [List Keysets](actions/list-keysets.md) | GET | Retrieves keysets from PubNub. |
| [Update Keyset](actions/update-keyset.md) | PUT | Updates an existing keyset in PubNub. |

### Keyset Configuration

| Action | Method | Description |
| --- | --- | --- |
| [Get Keyset Configuration](actions/get-keyset-configuration.md) | GET | Retrieves keyset configuration from PubNub. |
| [Update Keyset Configuration](actions/update-keyset-configuration.md) | PUT | Updates keyset configuration in PubNub. |

### Metrics

| Action | Method | Description |
| --- | --- | --- |
| [List Metrics](actions/list-metrics.md) | GET | Retrieves metrics from PubNub Illuminate. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Create Business Object](actions/create-business-object.md) | POST | Creates a business object in PubNub Illuminate. |
| [Issue Customer Access Token](actions/issue-customer-access-token.md) | POST | Issues a customer access token in PubNub. |

### Queries

| Action | Method | Description |
| --- | --- | --- |
| [List Queries](actions/list-queries.md) | GET | Retrieves queries from PubNub Illuminate. |

### Secret Key

| Action | Method | Description |
| --- | --- | --- |
| [Delete Rotated Secret Key](actions/delete-rotated-secret-key.md) | DELETE | Deletes a rotated secret key from PubNub. |
| [List Secret Keys For Keyset](actions/list-secret-keys-for-keyset.md) | GET | Retrieves secret keys for a PubNub keyset. |
| [Rotate Secret Key](actions/rotate-secret-key.md) | PUT | Rotates a secret key for a PubNub keyset. |
| [Update Secret Key Expiration Time](actions/update-secret-key-expiration-time.md) | PUT | Updates secret key expiration time in PubNub. |

### Usage Metric

| Action | Method | Description |
| --- | --- | --- |
| [Get Usage Metrics](actions/get-usage-metrics.md) | GET | Retrieves usage metrics from PubNub. |

