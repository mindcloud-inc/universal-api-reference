# Search Modified Inspections with SafetyCulture

Finds modified inspections in SafetyCulture.

## Endpoint

- **Method:** `GET`
- **Path:** `/audits/search`
- **Base URL:** `https://api.safetyculture.io`
- **Official documentation:** [Search Modified Inspections](https://developer.safetyculture.com/reference/thepubservice_searchinspections)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `field` | query | `string` | no | The fields to return. Defaults to just `audit_id`.   - audit_id: Include `audit_id` in the response.  - modified_at: Include `modified_at` in the response.  - template_id: Include `template_id` in the response. Send multiple values as a array. |
| `order` | query | `string` | no | The order to return results in.   - asc: Ascending order.  - desc: Descending order. |
| `modified_after` | query | `date` | no | Filter inspections modified after this date time. |
| `modified_before` | query | `date` | no | Filter inspections modified before this date time. |
| `template` | query | `string` | no | Filter to inspections conducted from these templates. Send multiple values as a array. |
| `archived` | query | `string` | no | Filter results by archived status. Default is `false`.   - false: Only unarchived inspections.  - true: Only archived inspections.  - both: Both unarchived and archived inspections. |
| `completed` | query | `string` | no | Filter results by completed status. Default is `both`.   - both: Both complete and incomplete inspections.  - false: Only incomplete inspections.  - true: Only complete inspections. |
| `owner` | query | `string` | no | Filter results by owner. Default is `all`.   - all: Owned by anyone.  - me: Only owned by the requesting user  - other: Only owned by other users. |
| `limit` | query | `number` | no | Limit the number of results returned. Default is `100`. |
