# Get Transactional Message Deliveries with Customer.io

Retrieves deliveries for a Customer.io transactional message.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/transactional/:transactional_id/messages`
- **Base URL:** `https://api.customer.io`
- **Official documentation:** [Get Transactional Message Deliveries](https://docs.customer.io/integrations/api/app/#tag/Transactional/operation/transactionalMessages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transactional_id` | path | `number` | yes | The identifier of your transactional message. |
| `limit` | query | `number` | no | The maximum number of results you want to retrieve per page. |
| `metric` | query | `list<string>` | no | Determines the metric you want to return. Accepted values: `attempted`, `bounced`, `clicked`, `converted`, `delivered`, `dropped`, `failed`, `opened`, `sent`, `spammed`, `undeliverable`, `unsubscribed`. |
| `state` | query | `list<string>` | no | The state of the delivery set you want to return. Accepted values: `attempted`, `drafted`, `failed`, `sent`. |
| `start_ts` | query | `number` | no | The beginning timestamp for your query. |
| `end_ts` | query | `number` | no | The ending timestamp for your query. |
| `start` | query | `string` | no | The token for the page of results you want to return. |
