# Retrieve Delivery Status Updates with boomApp Connect

Retrieves outbound delivery status updates from boomApp Connect.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/get_all_new_drs`
- **Base URL:** `https://direct-api.apps.boomcomms.com`
- **Official documentation:** [Retrieve Delivery Status Updates](https://github.com/microsoft/PowerPlatformConnectors/blob/dev/certified-connectors/BoomappConnect/apiDefinition.swagger.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `drs_after` | query | `string` | yes | Required by the Boomerang API when retrieving delivery receipts. Use format YYYY-MM-DD HH:MM:SS. |
| `start_transaction_id` | query | `number` | no | Return delivery receipts from this transaction ID onward. |
| `ignore_previous` | query | `boolean` | no | Exclude previously retrieved delivery receipts. |
