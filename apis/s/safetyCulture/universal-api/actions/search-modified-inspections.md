# SafetyCulture: Search Modified Inspections

Finds modified inspections in SafetyCulture.

```
GET https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/search-modified-inspections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SafetyCulture `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/search-modified-inspections?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/search-modified-inspections?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `field` | string | no | The fields to return. Defaults to just `audit_id`. - audit_id: Include `audit_id` in the response. - modified_at: Include `modified_at` in the response. - template_id: Include `template_id` in the response. Accepts multiple values as an array. |
| `order` | string | no | The order to return results in. - asc: Ascending order. - desc: Descending order. |
| `modifiedAfter` | date | no | Filter inspections modified after this date time. |
| `modifiedBefore` | date | no | Filter inspections modified before this date time. |
| `template` | string | no | Filter to inspections conducted from these templates. Accepts multiple values as an array. |
| `archived` | string | no | Filter results by archived status. Default is `false`. - false: Only unarchived inspections. - true: Only archived inspections. - both: Both unarchived and archived inspections. |
| `completed` | string | no | Filter results by completed status. Default is `both`. - both: Both complete and incomplete inspections. - false: Only incomplete inspections. - true: Only complete inspections. |
| `owner` | string | no | Filter results by owner. Default is `all`. - all: Owned by anyone. - me: Only owned by the requesting user - other: Only owned by other users. |
| `limit` | number | no | Limit the number of results returned. Default is `100`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "auditId": "string",
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "templateId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `auditId` | string |  |
| `modifiedAt` | date |  |
| `templateId` | string |  |

## Native endpoint

Through the native SafetyCulture API, this operation is `GET /audits/search` (base URL `https://api.safetyculture.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-modified-inspections.md) for the provider-specific parameters and requirements.

