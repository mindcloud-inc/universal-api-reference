# Search Modified Templates with SafetyCulture

Finds modified templates in SafetyCulture.

## Endpoint

- **Method:** `GET`
- **Path:** `/templates/search`
- **Base URL:** `https://api.safetyculture.io`
- **Official documentation:** [Search Modified Templates](https://developer.safetyculture.com/reference/thepubservice_searchtemplates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Limit the number of results returned. Default is `1000`. |
| `field` | query | `string` | no | The fields to return. Defaults to just `audit_id`.   - template_id: Include `template_id` in the response.  - name: Include `name` in the response.  - modified_at: Include `modified_at` in the response.  - created_at: Include `modified_at` in the response. Send multiple values as a array. |
| `order` | query | `string` | no | The order to return results in.   - asc: Order by `modified_at` in ascending order.  - desc: Order by `modified_at` in descending order. |
| `modified_after` | query | `date` | no | Filter results modified after this date time. |
| `modified_before` | query | `date` | no | Filter results modified before this date time. |
| `archived` | query | `string` | no | Filter results by archived status.   - false: Only include unarchived templates.  - true: Only include archived templates.  - both: Include both archived and unarchived templates. |
| `owner` | query | `string` | no | Filter results by owner.   - all: Include all templates.  - me: Only include templates owned by the requesting user.  - other: Only include templates owned by other users. |
