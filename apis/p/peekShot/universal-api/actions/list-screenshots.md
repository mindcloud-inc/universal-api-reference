# PeekShot: List Screenshots

Retrieves screenshots from PeekShot with optional filtering.

```
GET https://connect.mindcloud.co/v1/universal/peekShot/latest/actions/list-screenshots
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PeekShot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/peekShot/latest/actions/list-screenshots?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/peekShot/latest/actions/list-screenshots?${params}`, {
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
| `projectId` | string | no | Filter by project ID. |
| `url` | string | no | Filter by captured URL. |
| `status` | string | no | Filter by screenshot status: PENDING, COMPLETE, or FAILED. |
| `page` | string | no | Page number for paginated results. |
| `limit` | string | no | Number of results per page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "meta": {
          "currentPage": 1,
          "limit": 1,
          "totalScreenshots": 1
        },
        "screenshots": [
          {}
        ]
      },
      "message": "string",
      "status": "string",
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.meta.currentPage` | number | Current page number. |
| `data.meta.limit` | number | Page size applied to the result. |
| `data.meta.totalScreenshots` | number | Total screenshots matching the query. |
| `data.screenshots` | array<object> | Screenshot records returned by PeekShot. |
| `message` | string | Provider message. |
| `status` | string | Request status. |
| `statusCode` | number | HTTP-style status code returned by the provider. |

## Native endpoint

Through the native PeekShot API, this operation is `GET /screenshots` (base URL `https://api.peekshot.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-screenshots.md) for the provider-specific parameters and requirements.

