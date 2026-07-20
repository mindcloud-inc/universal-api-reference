# <img src="https://images.mindcloud.co/apps/icons/idue-fc-4cc-1774284757231_1774284765081.jpeg" alt="Detrack logo" width="28" height="28"> Detrack: Universal API

Manage delivery jobs, routes, depots, tracking, and proof of delivery

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/detrack/latest
- **Category:** Commerce / Supply Chain
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.detrack.com
- **Vendor API docs:** https://detrackapiv2.docs.apiary.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Depots](actions/list-depots.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/detrack/latest/actions/list-depots?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Depot

| Action | Method | Description |
| --- | --- | --- |
| [List Depots](actions/list-depots.md) | GET | Retrieves a list of depots from Detrack. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Batch Create Jobs](actions/batch-create-jobs.md) | POST | Creates multiple jobs in Detrack at once. |
| [Batch Delete Jobs](actions/batch-delete-jobs.md) | DELETE | Deletes multiple jobs from Detrack at once. |
| [Batch Update Jobs](actions/batch-update-jobs.md) | PUT | Updates multiple jobs in Detrack at once. |
| [Create Job](actions/create-job.md) | POST | Creates a new job in Detrack. |
| [Reattempt Job](actions/reattempt-job.md) | PUT | Reattempts a failed job in Detrack. |

### Job Export

| Action | Method | Description |
| --- | --- | --- |
| [Export Job By D.O. Number](actions/export-job-by-do-number.md) | GET | Exports a job document from Detrack by D.O. number. |
| [Export Job By D.O. Number And Date](actions/export-job-by-do-number-and-date.md) | GET | Exports a job document from Detrack by D.O. number and date. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Create Depots](actions/bulk-create-depots.md) | POST | Creates multiple depots in Detrack at once. |
| [Bulk Delete Depots](actions/bulk-delete-depots.md) | DELETE | Deletes multiple depots from Detrack at once. |
| [Bulk Update Depots](actions/bulk-update-depots.md) | PUT | Updates multiple depots in Detrack at once. |
| [Create Depot](actions/create-depot.md) | POST | Creates a new depot in Detrack. |
| [Delete Job By D.O. Number](actions/delete-job-by-do-number.md) | DELETE | Deletes an existing job from Detrack by D.O. number. |
| [Delete Job By D.O. Number And Date](actions/delete-job-by-do-number-and-date.md) | DELETE | Deletes an existing job from Detrack by D.O. number and date. |
| [List Depots By Name](actions/list-depots-by-name.md) | GET | Finds depots in Detrack by depot name. |
| [List Jobs](actions/list-jobs.md) | GET | Retrieves jobs from Detrack with optional filters. |
| [Retrieve Job By D.O. Number](actions/retrieve-job-by-do-number.md) | GET | Retrieves a job from Detrack by D.O. number. |
| [Retrieve Job By D.O. Number And Date](actions/retrieve-job-by-do-number-and-date.md) | GET | Retrieves a job from Detrack by D.O. number and date. |
| [Search Jobs](actions/search-jobs.md) | GET | Finds jobs in Detrack by search criteria. |
| [Update Job By D.O. Number](actions/update-job-by-do-number.md) | PUT | Updates an existing job in Detrack by D.O. number. |
| [Update Job By D.O. Number And Date](actions/update-job-by-do-number-and-date.md) | PUT | Updates an existing job in Detrack by D.O. number and date. |

### Route

| Action | Method | Description |
| --- | --- | --- |
| [List Routes By Date](actions/list-routes-by-date.md) | GET | Retrieves routes from Detrack for a specific date. |
| [List Routes By Name](actions/list-routes-by-name.md) | GET | Finds routes in Detrack by route name and date. |

