# List Service Accounts with Harness

Retrieves service accounts from Harness.

## Endpoint

- **Method:** `GET`
- **Path:** `/ng/api/serviceaccount`
- **Base URL:** `https://app.harness.io/gateway`
- **Official documentation:** [List Service Accounts](https://apidocs.harness.io/service-account/listserviceaccount)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifiers` | query | `list<string>` | no | Service account identifiers to include. |
