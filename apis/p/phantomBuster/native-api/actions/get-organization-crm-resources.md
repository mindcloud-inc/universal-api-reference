# Get Organization CRM Resources with PhantomBuster

Retrieves organization CRM resources from PhantomBuster.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs/fetch-crm-resources`
- **Base URL:** `https://api.phantombuster.com/api/v2`
- **Official documentation:** [Get Organization CRM Resources](https://hub.phantombuster.com/reference/get_orgs-fetch-crm-resources)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resourceType` | query | `list` | yes | Type of CRM resource to fetch. Allowed values: account_info, contact_lists, contact_properties. Accepted values: `account_info`, `contact_lists`, `contact_properties`. |
