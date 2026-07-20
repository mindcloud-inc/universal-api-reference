# Kazm: List Transform Jobs

Retrieves transform jobs from Kazm.

```
GET https://connect.mindcloud.co/v1/universal/kazm/latest/actions/list-transform-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kazm `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kazm/latest/actions/list-transform-jobs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kazm/latest/actions/list-transform-jobs?${params}`, {
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
| `cursor` | string | no | Cursor for the next page of transform jobs. |
| `limit` | string | no | Maximum number of transform jobs to return. |
| `status` | string | no | Filter transform jobs by status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "has_more": true,
      "jobs": [
        {}
      ],
      "next_cursor": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `has_more` | boolean |  |
| `jobs` | array<object> |  |
| `next_cursor` | string |  |
| `total` | number |  |

## Native endpoint

Through the native Kazm API, this operation is `GET /transform-jobs` (base URL `https://api.lightningrod.ai/api/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-transform-jobs.md) for the provider-specific parameters and requirements.

