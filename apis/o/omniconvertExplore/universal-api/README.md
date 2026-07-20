# <img src="https://images.mindcloud.co/apps/icons/omniconvert-explore_1774879907723.png" alt="Omniconvert Explore logo" width="28" height="28"> Omniconvert Explore: Universal API

Run experiments and analyze website stats, growth, and segments

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/omniconvertExplore/latest
- **Category:** Marketing
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.omniconvert.com
- **Vendor API docs:** https://api.omniconvert.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Websites](actions/list-websites.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/omniconvertExplore/latest/actions/list-websites?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Connection

| Action | Method | Description |
| --- | --- | --- |
| [Validate Account](actions/validate-account.md) | GET | Retrieves account validation details from Omniconvert Explore. |

### Experiment

| Action | Method | Description |
| --- | --- | --- |
| [Get Experiment](actions/get-experiment.md) | GET | Retrieves an experiment from Omniconvert Explore. |
| [Get Experiment Stats](actions/get-experiment-stats.md) | GET | Retrieves experiment statistics from Omniconvert Explore. |
| [List Active Experiments](actions/list-active-experiments.md) | GET | Retrieves active experiments from Omniconvert Explore. |
| [List Experiments](actions/list-experiments.md) | GET | Retrieves experiments for a website from Omniconvert Explore. |
| [Start or Stop Experiment](actions/start-or-stop-experiment.md) | PUT | Updates an experiment by starting or stopping it in Omniconvert Explore. |

### Segment

| Action | Method | Description |
| --- | --- | --- |
| [Delete Segment](actions/delete-segment.md) | DELETE | Deletes an existing segment from Omniconvert Explore. |
| [Get Segment](actions/get-segment.md) | GET | Retrieves a segment from Omniconvert Explore. |
| [List Segments](actions/list-segments.md) | GET | Retrieves account segments from Omniconvert Explore. |

### Website

| Action | Method | Description |
| --- | --- | --- |
| [Get Website Growth](actions/get-website-growth.md) | GET | Retrieves website growth metrics from Omniconvert Explore. |
| [Get Website Stats](actions/get-website-stats.md) | GET | Retrieves website statistics from Omniconvert Explore. |
| [List Websites](actions/list-websites.md) | GET | Retrieves account websites from Omniconvert Explore. |

