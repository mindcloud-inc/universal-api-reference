# Kadoa: Get Change



```
GET https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/get-change
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kadoa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/get-change?connectionId=$CONNECTION_ID&changeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "changeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/get-change?${params}`, {
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
| `changeId` | string | yes | Change ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "changes": [
        {}
      ],
      "changesCount": 1,
      "pagination": {
        "limit": 1,
        "page": 1,
        "totalCount": 1,
        "totalPages": 1
      },
      "timestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `changes` | array<object> |  |
| `changesCount` | number |  |
| `pagination.limit` | number |  |
| `pagination.page` | number |  |
| `pagination.totalCount` | number |  |
| `pagination.totalPages` | number |  |
| `timestamp` | date |  |

## Native endpoint

Through the native Kadoa API, this operation is `GET /v4/changes/:changeId` (base URL `https://api.kadoa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-change.md) for the provider-specific parameters and requirements.

