# LambdaTest: List Builds

Retrieves builds from LambdaTest.

```
GET https://connect.mindcloud.co/v1/universal/lambdaTest/latest/actions/list-builds
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LambdaTest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lambdaTest/latest/actions/list-builds?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lambdaTest/latest/actions/list-builds?${params}`, {
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
| `limit` | number | no | Maximum number of builds to return. |
| `offset` | number | no | Number of builds to skip before returning results. |
| `status` | string | no | Comma-separated LambdaTest build statuses to filter by. |
| `fromDate` | string | no | Start date in YYYY-MM-DD format. |
| `toDate` | string | no | End date in YYYY-MM-DD format. |
| `sort` | string | no | Sort expression such as asc.user_id or desc.end_time. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "message": "string",
      "Meta": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Builds returned by the query. |
| `message` | string | LambdaTest status message. |
| `Meta` | object | Pagination and organization metadata. |
| `status` | string | Request status. |

## Native endpoint

Through the native LambdaTest API, this operation is `GET /builds` (base URL `https://api.lambdatest.com/automation/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-builds.md) for the provider-specific parameters and requirements.

