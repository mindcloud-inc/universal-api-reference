# Get Application Details with New Relic

Retrieves application details from New Relic.

## Endpoint

- **Method:** `GET`
- **Path:** `/applications/:appId.json`
- **Base URL:** `https://api.newrelic.com/v2`
- **Official documentation:** [Get Application Details](https://docs.newrelic.com/docs/apis/rest-api-v2/application-examples-v2/summary-data-examples-v2/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | path | `number` | yes | New Relic application ID. |
