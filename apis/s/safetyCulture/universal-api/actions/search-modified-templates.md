# SafetyCulture: Search Modified Templates

Finds modified templates in SafetyCulture.

```
GET https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/search-modified-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SafetyCulture `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/search-modified-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/search-modified-templates?${params}`, {
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
| `limit` | number | no | Limit the number of results returned. Default is `1000`. |
| `field` | string | no | The fields to return. Defaults to just `audit_id`. - template_id: Include `template_id` in the response. - name: Include `name` in the response. - modified_at: Include `modified_at` in the response. - created_at: Include `modified_at` in the response. Accepts multiple values as an array. |
| `order` | string | no | The order to return results in. - asc: Order by `modified_at` in ascending order. - desc: Order by `modified_at` in descending order. |
| `modifiedAfter` | date | no | Filter results modified after this date time. |
| `modifiedBefore` | date | no | Filter results modified before this date time. |
| `archived` | string | no | Filter results by archived status. - false: Only include unarchived templates. - true: Only include archived templates. - both: Include both archived and unarchived templates. |
| `owner` | string | no | Filter results by owner. - all: Include all templates. - me: Only include templates owned by the requesting user. - other: Only include templates owned by other users. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "templateId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `modifiedAt` | date |  |
| `name` | string |  |
| `templateId` | string |  |

## Native endpoint

Through the native SafetyCulture API, this operation is `GET /templates/search` (base URL `https://api.safetyculture.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-modified-templates.md) for the provider-specific parameters and requirements.

