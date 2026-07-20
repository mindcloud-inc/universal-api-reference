# <img src="https://images.mindcloud.co/apps/icons/city-of-tampa-florida_1776452708369.png" alt="City of Tampa, Florida logo" width="28" height="28"> City of Tampa, Florida: Universal API

Browse Tampa events, news, meetings, and public service feeds

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cityOfTampaFlorida/latest
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.tampa.gov/
- **Vendor API docs:** https://www.tampa.gov/info/rss-feeds

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Collection](actions/get-collection.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cityOfTampaFlorida/latest/actions/get-collection?connectionId=$CONNECTION_ID&collectionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Calendar Feed Item

| Action | Method | Description |
| --- | --- | --- |
| [List Calendar Feed Items](actions/list-calendar-feed-items.md) | GET | Retrieves calendar feed items from City of Tampa, Florida. |

### Collection Aggregation

| Action | Method | Description |
| --- | --- | --- |
| [Get Collection Aggregations](actions/get-collection-aggregations.md) | GET | Retrieves collection aggregations from City of Tampa, Florida. |

### Collection Item

| Action | Method | Description |
| --- | --- | --- |
| [Get Collection Item](actions/get-collection-item.md) | GET | Retrieves a collection item from City of Tampa, Florida. |
| [List Collection Items](actions/list-collection-items.md) | GET | Retrieves collection items from City of Tampa, Florida. |

### Connected Record

| Action | Method | Description |
| --- | --- | --- |
| [List Connected Records](actions/list-connected-records.md) | GET | Retrieves connected records from City of Tampa, Florida. |

### Construction Project News Item

| Action | Method | Description |
| --- | --- | --- |
| [List Construction Project News Feed Items](actions/list-construction-project-news-feed-items.md) | GET | Retrieves construction project news feed items from City of Tampa, Florida. |

### Contract Administration News Item

| Action | Method | Description |
| --- | --- | --- |
| [List Contract Administration News Feed Items](actions/list-contract-administration-news-feed-items.md) | GET | Retrieves contract administration news feed items from City of Tampa, Florida. |

### Data Collection

| Action | Method | Description |
| --- | --- | --- |
| [Get Collection](actions/get-collection.md) | GET | Retrieves a data collection from City of Tampa, Florida. |
| [List Data Collections](actions/list-data-collections.md) | GET | Retrieves data collections from City of Tampa, Florida. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [List All Events](actions/list-all-events.md) | GET | Retrieves all events from City of Tampa, Florida. |
| [List Events By Type](actions/list-events-by-type.md) | GET | Retrieves events by type from City of Tampa, Florida. |

### Event Type

| Action | Method | Description |
| --- | --- | --- |
| [List Event Types](actions/list-event-types.md) | GET | Retrieves event types from City of Tampa, Florida. |

### Job Opening

| Action | Method | Description |
| --- | --- | --- |
| [List Job Openings](actions/list-job-openings.md) | GET | Retrieves job openings from City of Tampa, Florida. |

### News Item

| Action | Method | Description |
| --- | --- | --- |
| [List News Feed Items](actions/list-news-feed-items.md) | GET | Retrieves news feed items from City of Tampa, Florida. |

### Police Event

| Action | Method | Description |
| --- | --- | --- |
| [List Police Events](actions/list-police-events.md) | GET | Retrieves police events from City of Tampa, Florida. |

### Police News Item

| Action | Method | Description |
| --- | --- | --- |
| [List Police News Feed Items](actions/list-police-news-feed-items.md) | GET | Retrieves police news feed items from City of Tampa, Florida. |

### Queryable Field

| Action | Method | Description |
| --- | --- | --- |
| [Get Collection Queryables](actions/get-collection-queryables.md) | GET | Retrieves collection queryable fields from City of Tampa, Florida. |

### Related Record

| Action | Method | Description |
| --- | --- | --- |
| [List Related Records](actions/list-related-records.md) | GET | Retrieves related records from City of Tampa, Florida. |

### Search Api Capability

| Action | Method | Description |
| --- | --- | --- |
| [Get Search API Conformance](actions/get-search-api-conformance.md) | GET | Retrieves Search API conformance details from City of Tampa, Florida. |

### Search Catalog

| Action | Method | Description |
| --- | --- | --- |
| [Get Search Catalog](actions/get-search-catalog.md) | GET | Retrieves the search catalog from City of Tampa, Florida. |

