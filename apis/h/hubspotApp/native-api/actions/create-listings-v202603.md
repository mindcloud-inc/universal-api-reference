# Create Listings (v2026-03) with HubSpot

Creates a listing in HubSpot.

## Endpoint

- **Method:** `POST`
- **Path:** `crm/objects/2026-03/listings`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Create Listings (v2026-03)](https://developers.hubspot.com/docs/api-reference/crm-companies-v3/basic/patch-crm-v3-objects-companies-companyId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `properties` | body | `object` | yes | Object of company properties to update, e.g. {"arr":"250000"}. |
| `associations[]` | body | `array<object>` | no | ### Associations  Use this field to associate the new Listing with existing HubSpot records, such as contacts, companies, deals, or other supported CRM objects.  Provide an array of association objects using the following structure:  ```json [   {     "to": {       "id": "123456789"     },     "types": [       {         "associationCategory": "HUBSPOT_DEFINED",         "associationTypeId": 882       }     ]   } ] ```  Each association must include:  * `to.id`: The HubSpot record ID of the existing record you want to associate with the new Listing. * `types`: An array describing the relationship between the Listing and the associated record. * `associationCategory`: Use `HUBSPOT_DEFINED` for standard HubSpot associations or `USER_DEFINED` for custom association labels. * `associationTypeId`: The numeric ID of the association type or label.  You may include multiple objects in the array to associate the Listing with more than one record.  Example with multiple associations:  ```json [   {     "to": {       "id": "123456789"     },     "types": [       {         "associationCategory": "HUBSPOT_DEFINED",         "associationTypeId": 882       }     ]   },   {     "to": {       "id": "987654321"     },     "types": [       {         "associationCategory": "HUBSPOT_DEFINED",         "associationTypeId": 884       }     ]   } ] ```  The correct `associationTypeId` depends on the target object type and association label configured in the connected HubSpot account. |
