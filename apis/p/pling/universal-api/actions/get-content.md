# Pling: Get Content

Retrieves public content details from Pling.

```
GET https://connect.mindcloud.co/v1/universal/pling/latest/actions/get-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pling/latest/actions/get-content?connectionId=$CONNECTION_ID&contentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pling/latest/actions/get-content?${params}`, {
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
| `contentId` | string | yes | Pling content identifier to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "changed": "2026-05-07T12:00:00.000Z",
      "created": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "detailpage": "string",
      "downloads": 1,
      "id": "string",
      "name": "Ava Chen",
      "personid": "string",
      "score": 1,
      "summary": "string",
      "typename": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `changed` | date | Last update timestamp. |
| `created` | date | Creation timestamp. |
| `description` | string | Full content description. |
| `detailpage` | string | Pling detail page URL. |
| `downloads` | number | Download count. |
| `id` | string | Content identifier. |
| `name` | string | Content title. |
| `personid` | string | Publishing username. |
| `score` | number | Provider score. |
| `summary` | string | Short content summary. |
| `typename` | string | Content type display name. |

## Native endpoint

Through the native Pling API, this operation is `GET /content/data/:contentId` (base URL `https://api.pling.com/ocs/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-content.md) for the provider-specific parameters and requirements.

