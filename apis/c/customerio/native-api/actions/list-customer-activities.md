# List Customer Activities with Customer.io

Retrieves activities for a customer in Customer.io.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/customers/:customer_id/activities`
- **Base URL:** `https://api.customer.io`
- **Official documentation:** [List Customer Activities](https://docs.customer.io/integrations/api/app/#tag/Customers/operation/getPersonActivities)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_id` | path | `string` | yes | The ID of the customer you want to inspect. |
| `id_type` | query | `list<string>` | no | The type of customer identifier supplied in Customer ID. Accepted values: `cio_id`, `email`, `id`. |
| `limit` | query | `number` | no | The maximum number of results you want to retrieve per page. |
| `type` | query | `string` | no | The type of activity you want to search for. |
| `name` | query | `string` | no | For event and attribute_update types, search by event or attribute name. |
| `start` | query | `string` | no | The token for the page of results you want to return. |
