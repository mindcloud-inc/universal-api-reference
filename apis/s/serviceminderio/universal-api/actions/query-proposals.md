# serviceminder.io: Query Proposals

Finds proposals in ServiceMinder by date range.

```
GET https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/query-proposals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a serviceminder.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/query-proposals?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serviceminderio/latest/actions/query-proposals?${params}`, {
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
| `fromDate` | string | no | Start date for proposal query. |
| `throughDate` | string | no | End date for proposal query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "message": "string",
      "proposals": [
        {}
      ],
      "resultCode": 1,
      "scope": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `message` | string |  |
| `proposals` | array<object> |  |
| `resultCode` | number |  |
| `scope` | string |  |

## Native endpoint

Through the native serviceminder.io API, this operation is `POST /proposal/query` (base URL `https://serviceminder.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-proposals.md) for the provider-specific parameters and requirements.

