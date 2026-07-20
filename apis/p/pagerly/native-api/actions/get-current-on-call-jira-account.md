# Get Current On-Call Jira Account with Pagerly

Retrieves the current on-call Jira account from Pagerly.

## Endpoint

- **Method:** `GET`
- **Path:** `/o/currentusersforjira`
- **Base URL:** `https://api.pagerly.io/pagerly`
- **Official documentation:** [Get Current On-Call Jira Account](https://docs.pagerly.io/fetch-current-oncall-rotated-user-via-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamname` | query | `string` | yes | Exact Pagerly team name to resolve to a Jira accountId. |
