# Get Key Transaction with New Relic

Retrieves a key transaction from New Relic.

## Endpoint

- **Method:** `GET`
- **Path:** `/key_transactions/:keyTransactionId.json`
- **Base URL:** `https://api.newrelic.com/v2`
- **Official documentation:** [Get Key Transaction](https://docs.newrelic.com/docs/apis/rest-api-v2/application-examples-v2/summary-data-examples-v2/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keyTransactionId` | path | `number` | yes | New Relic key transaction ID. |
