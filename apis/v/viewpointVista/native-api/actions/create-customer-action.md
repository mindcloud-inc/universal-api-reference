# Create Customer Action with Viewpoint Vista

## Endpoint

- **Method:** `POST`
- **Path:** `v1/direct/subscribers/:subscriber_code/vista/:api/2/data/customers/actions/add`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Create Customer Action](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistaar2datacustomersactionsadd)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ARCo` | body | `number` | no |
| `Customer` | body | `object` | no |
| `Name` | body | `string` | no |
| `MailingAddress` | body | `object` | no |
| `BillingAddress` | body | `object` | no |
| `PayTerms` | body | `string` | no |
| `CompanyContact` | body | `object` | no |
| `__custom_fields` | body | `object` | no |
