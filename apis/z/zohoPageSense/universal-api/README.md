# <img src="https://images.mindcloud.co/apps/icons/zoho-page-sense_1774035102349.png" alt="Zoho PageSense logo" width="28" height="28"> Zoho PageSense: Universal API

Track goals, analyze behavior, and run website experiments

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zohoPageSense/latest
- **Category:** Marketing
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pagesense.zoho.com
- **Vendor API docs:** https://www.zoho.com/pagesense/developerguide/apidocs/absplittestoverview.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Project Goals](actions/get-project-goals.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoPageSense/latest/actions/get-project-goals?connectionId=$CONNECTION_ID&portalName=Ava%20Chen&projectLinkname=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Audience

| Action | Method | Description |
| --- | --- | --- |
| [List Predefined & Custom Audiences](actions/list-predefined-custom-audiences.md) | GET | Retrieves predefined and custom audiences from Zoho PageSense. |
| [List Selected Audiences](actions/list-selected-audiences.md) | GET | Retrieves selected audiences from Zoho PageSense. |
| [Update Experiment Audience](actions/update-experiment-audience.md) | PUT | Updates experiment audience settings in Zoho PageSense. |

### Custom Event

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Event](actions/create-custom-event.md) | POST | Creates a custom event in Zoho PageSense. |
| [List Custom Events](actions/list-custom-events.md) | GET | Retrieves custom events from Zoho PageSense. |

### Experiment

| Action | Method | Description |
| --- | --- | --- |
| [Create Experiment](actions/create-experiment.md) | POST | Creates an experiment in Zoho PageSense. |
| [Get Experiment Details](actions/get-experiment-details.md) | GET | Retrieves experiment details from Zoho PageSense. |
| [Publish Experiment](actions/publish-experiment.md) | PUT | Publishes an experiment in Zoho PageSense. |
| [Update Experiment Variations](actions/update-experiment-variations.md) | PUT | Updates experiment variations in Zoho PageSense. |

### Goal

| Action | Method | Description |
| --- | --- | --- |
| [Create Goal for Experiment](actions/create-goal-for-experiment.md) | POST | Creates an experiment goal in Zoho PageSense. |
| [Create Project Goal](actions/create-project-goal.md) | POST | Creates a project goal in Zoho PageSense. |
| [Delete Goal for Experiment](actions/delete-goal-for-experiment.md) | DELETE | Deletes an experiment goal from Zoho PageSense. |
| [Delete Project Goal](actions/delete-project-goal.md) | DELETE | Deletes a project goal from Zoho PageSense. |
| [Get Project Goals](actions/get-project-goals.md) | GET | Retrieves project goals from Zoho PageSense. |
| [Update Goal for Experiment](actions/update-goal-for-experiment.md) | PUT | Updates an experiment goal in Zoho PageSense. |
| [Update Project Goal](actions/update-project-goal.md) | PUT | Updates an existing project goal in Zoho PageSense. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Day-Wise Stats Reports](actions/day-wise-stats-reports.md) | GET | Retrieves day-wise stats reports from Zoho PageSense. |
| [Individual Stats Report](actions/individual-stats-report.md) | GET | Retrieves an individual stats report from Zoho PageSense. |
| [Total Stats Report](actions/total-stats-report.md) | GET | Retrieves a total stats report from Zoho PageSense. |

