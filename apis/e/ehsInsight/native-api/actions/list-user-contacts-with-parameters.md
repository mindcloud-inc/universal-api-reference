# List User Contacts with Parameters with EHS Insight

## Endpoint

- **Method:** `GET`
- **Path:** `/v6/entity/UserContact/list`
- **Base URL:** `https://{companyName}.ehsinsight.com/api`
- **Official documentation:** [List User Contacts with Parameters](https://qxobptest.ehsinsight.com/site#/apidocumentation/v6/apidoc_entityapi_list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | query | `string` | no | Comma-separated root-level fields to return. Related captions may be requested with dot notation. This does not fetch the full record. |
| `updatedBefore` | query | `date` | no | Return records modified before this UTC date/time. |
| `updatedAfter` | query | `date` | no | Return records modified after this UTC date/time. |
| `createdBefore` | query | `date` | no | Return records created before this UTC date/time. |
| `createdAfter` | query | `date` | no | Return records created after this UTC date/time. |
| `changeTokenBefore` | query | `string` | no | Return records with a change token before this token. |
| `changeTokenAfter` | query | `string` | no | Return newer records ordered by change token ascending. Use the last returned token for the next call. |
