# Update DNS Record with Vercel

Updates an existing DNS record in Vercel.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/domains/records/:recordId`
- **Base URL:** `https://api.vercel.com`
- **Official documentation:** [Update DNS Record](https://docs.vercel.com/docs/rest-api/reference/endpoints/dns/update-an-existing-dns-record)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | The updated DNS record name. |
| `recordId` | path | `string` | yes | The DNS record ID to update. |
| `type` | body | `string` | no | The updated DNS record type. |
| `value` | body | `string` | no | The updated DNS record value. |
