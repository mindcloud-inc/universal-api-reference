# Cituro: List Ratings

Retrieves a list of ratings from Cituro.

```
GET https://connect.mindcloud.co/v1/universal/cituro/latest/actions/list-ratings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cituro `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cituro/latest/actions/list-ratings?connectionId=$CONNECTION_ID&accountNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cituro/latest/actions/list-ratings?${params}`, {
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
| `accountNumber` | string | yes | The Cituro account number used in the ratings endpoint path. |
| `limit` | number | no | Maximum number of ratings to return. |
| `sort` | string | no | Sort expression such as -createdAt for newest first. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "anonymous": true,
      "comment": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customerName": "Ava Chen",
      "rating": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `anonymous` | boolean | Whether the rating was submitted anonymously. |
| `comment` | string | Optional rating comment. |
| `createdAt` | date | Timestamp when the rating was created. |
| `customerName` | string | Customer display name for the rating when available. |
| `rating` | number | Rating value from 1 to 5 stars. |

## Native endpoint

Through the native Cituro API, this operation is `GET /ratings/:accountNumber` (base URL `https://app.cituro.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-ratings.md) for the provider-specific parameters and requirements.

