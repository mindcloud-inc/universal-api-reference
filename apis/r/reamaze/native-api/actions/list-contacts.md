# List Contacts with Reamaze

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://{brand}.reamaze.io/api/v1`
- **Official documentation:** [List Contacts](https://www.reamaze.com/api/get_contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | `q` with any string will search over contacts by name or email |
| `data[key]=value` | query | `string` | no | `data` with a hash of key/value pairs (e.g. `data[key]=value`) will return contacts with `data` matching those key/value pairs. |
| `sort` | query | `string` | no | `sort` with value set to `date` will return results in descending order of create time. The default sort when this parameter is not provided is by name. |
| `date` | query | `date` | no | `sort` with value set to `date` will return results in descending order of create time. The default sort when this parameter is not provided is by name. |
| `type` | query | `string` | no | `type` with values set to `email` or `mobile` will return only contacts that have an email address or phone number, respectively. |
| `email` | query | `string` | no | `type` with values set to `email` or `mobile` will return only contacts that have an email address or phone number, respectively. |
| `mobile` | query | `string` | no | `type` with values set to `email` or `mobile` will return only contacts that have an email address or phone number, respectively. |
