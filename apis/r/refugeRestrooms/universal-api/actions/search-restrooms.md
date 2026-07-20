# Refuge Restrooms: Search Restrooms



```
GET https://connect.mindcloud.co/v1/universal/refugeRestrooms/latest/actions/search-restrooms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Refuge Restrooms `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/refugeRestrooms/latest/actions/search-restrooms?connectionId=$CONNECTION_ID&limit=25&offset=0&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/refugeRestrooms/latest/actions/search-restrooms?${params}`, {
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
| `query` | string | yes | Full-text search query for restroom records. |
| `ada` | boolean | no | Only return restrooms that are ADA accessible. |
| `unisex` | boolean | no | Only return restrooms that are unisex. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `resultOffset` | number | no | Pad a number of results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessible": true,
      "approved": true,
      "changing_table": true,
      "city": "string",
      "comment": "string",
      "country": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "directions": "string",
      "downvote": 1,
      "edit_id": 1,
      "id": 1,
      "latitude": 1,
      "longitude": 1,
      "name": "Ava Chen",
      "state": "string",
      "street": "string",
      "unisex": true,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "upvote": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessible` | boolean |  |
| `approved` | boolean |  |
| `changing_table` | boolean |  |
| `city` | string |  |
| `comment` | string |  |
| `country` | string |  |
| `created_at` | date |  |
| `directions` | string |  |
| `downvote` | number |  |
| `edit_id` | number |  |
| `id` | number |  |
| `latitude` | number |  |
| `longitude` | number |  |
| `name` | string |  |
| `state` | string |  |
| `street` | string |  |
| `unisex` | boolean |  |
| `updated_at` | date |  |
| `upvote` | number |  |

## Native endpoint

Through the native Refuge Restrooms API, this operation is `GET /v1/restrooms/search` (base URL `https://www.refugerestrooms.org/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-restrooms.md) for the provider-specific parameters and requirements.

