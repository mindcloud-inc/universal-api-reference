# Streak: Search Boxes, Contacts, and Organizations

Finds boxes, contacts, and organizations in Streak by query.

```
GET https://connect.mindcloud.co/v1/universal/streak/latest/actions/search-boxes-contacts-and-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streak `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/streak/latest/actions/search-boxes-contacts-and-organizations?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/streak/latest/actions/search-boxes-contacts-and-organizations?${params}`, {
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
| `query` | string | yes | Search term used to find boxes, contacts, and organizations. |
| `pipelineKey` | string<string> | no | Limit box results to one or more pipelines. Accepts multiple values as an array. |
| `stageKey` | string<string> | no | Limit box results to one or more stages. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "page": 1,
      "query": "string",
      "results": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `page` | number | The current search results page. |
| `query` | string | The search term that was executed. |
| `results` | object | The search results grouped by boxes, contacts, and organizations. |

## Native endpoint

Through the native Streak API, this operation is `GET /api/v1/search` (base URL `https://api.streak.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-boxes-contacts-and-organizations.md) for the provider-specific parameters and requirements.

