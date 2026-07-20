# List Contacts with ActiveTrail

Retrieves a list of contacts from ActiveTrail.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://webapi.mymarketing.co.il/api`
- **Official documentation:** [List Contacts](https://webapi.mymarketing.co.il/api/docs/and/Api/GET-api-contacts_CustomerStates_SearchTerm_FromDate_ToDate_Page_Limit)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_states` | query | `list<string>` | yes | Choose the states of the contacts you want to get. Accepted values: `ACTIVE`, `ALL`, `BOUNCED`, `CUSTOMER_REQUEST`, `INACTIVE`, `QUARANTINED`, `SPAM_COMPLIENT`. |
| `from_date` | query | `date` | no | Only include contacts from this date forward. |
| `search_term` | query | `string` | no | Search contacts by a free-text term. |
| `to_date` | query | `date` | no | Only include contacts up to this date. |
