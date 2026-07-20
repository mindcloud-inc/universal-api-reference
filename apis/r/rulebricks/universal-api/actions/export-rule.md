# Rulebricks: Export Rule

Exports a rule from Rulebricks.

```
GET https://connect.mindcloud.co/v1/universal/rulebricks/latest/actions/export-rule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rulebricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rulebricks/latest/actions/export-rule?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rulebricks/latest/actions/export-rule?${params}`, {
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
| `id` | string | yes | ID of the rule to export |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "owner": "string",
      "published": true,
      "requestCount": 1,
      "runCount": 1,
      "sampleRequest": {},
      "sampleResponse": {},
      "slug": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Creation timestamp |
| `description` | string | Rule description |
| `id` | string | Rule ID |
| `name` | string | Rule name |
| `owner` | string | Owner ID |
| `published` | boolean | Whether the rule is published |
| `requestCount` | number | Request count |
| `runCount` | number | Run count |
| `sampleRequest` | object | Sample request object |
| `sampleResponse` | object | Sample response object |
| `slug` | string | Rule slug |
| `updatedAt` | date | Update timestamp |

## Native endpoint

Through the native Rulebricks API, this operation is `GET /admin/rules/export` (base URL `https://rulebricks.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-rule.md) for the provider-specific parameters and requirements.

