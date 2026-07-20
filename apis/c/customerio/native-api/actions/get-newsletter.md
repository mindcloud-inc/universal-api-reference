# Get Newsletter with Customer.io

Retrieves a newsletter from Customer.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/newsletters/:newsletter_id`
- **Base URL:** `https://api.customer.io`
- **Official documentation:** [Get Newsletter](https://docs.customer.io/integrations/api/app/#tag/Newsletters/operation/getNewsletters)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `newsletter_id` | path | `number` | yes | The numeric ID of the newsletter you want to retrieve. |
