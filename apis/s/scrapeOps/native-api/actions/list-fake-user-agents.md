# List Fake User Agents with ScrapeOps

Retrieves fake user agents from ScrapeOps.

## Endpoint

- **Method:** `GET`
- **Path:** `http://headers.scrapeops.io/v1/user-agents`
- **Base URL:** `http://headers.scrapeops.io/v1`
- **Official documentation:** [List Fake User Agents](https://scrapeops.io/docs/fake-user-agent-headers-api/fake-user-agents/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `num_results` | query | `number` | no | How many fake user agents to return. |
| `mobile` | query | `boolean` | no | Return mobile user agents only when true. |
