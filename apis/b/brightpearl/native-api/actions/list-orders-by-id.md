# List Orders by ID with Brightpearl

## Endpoint

- **Method:** `GET`
- **Path:** `/order-service/order/:orderIds`
- **Base URL:** `https://{apiDomain}/public-api/{account}`
- **Official documentation:** [List Orders by ID](https://api-docs.brightpearl.com/order/order/get.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `orderIds` | path | `string` | yes | One order ID, comma-separated IDs, or ID ranges such as 100-120,130. Request at most 200 orders per call; use Order OPTIONS for larger sets. |
| `includeOptional` | query | `list<string>` | no | Optional comma-separated sections: customFields,nullCustomFields. Accepted values: `customFields`, `nullCustomFields`. Send multiple values as a string separated by `,`. |
