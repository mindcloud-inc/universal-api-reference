# Get CRM Recording with Sipuni

## Endpoint

- **Method:** `GET`
- **Path:** `/crm/record`
- **Base URL:** `https://sipuni.com/api`
- **Official documentation:** [Get CRM Recording](https://doc.sipuni.com/articles/636-642--poluchenie-statistiki/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | CRM recording ID from a Sipuni CRM recording link. |
| `hash` | query | `string` | yes | Precomputed Sipuni CRM recording hash from the original call_record_link URL. |
