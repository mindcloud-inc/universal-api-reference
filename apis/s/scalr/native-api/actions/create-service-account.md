# Create Service Account with Scalr

Creates a new service account in Scalr.

## Endpoint

- **Method:** `POST`
- **Path:** `/service-accounts`
- **Base URL:** `https://mindcloud.scalr.io/api/iacp/v3`
- **Official documentation:** [Create Service Account](https://docs.scalr.io/reference/create_service_account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.attributes.name` | body | `string` | yes | Service account name. |
| `data.attributes.description` | body | `string` | no | Service account description. |
| `data.attributes.status` | body | `string` | no | Service account status. |
| `data.relationships.account.data.id` | body | `string` | yes | Related account ID. |
