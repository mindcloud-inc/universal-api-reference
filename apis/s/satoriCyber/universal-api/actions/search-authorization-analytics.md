# Satori Cyber: Search Authorization Analytics

Finds authorization analytics records in Satori Cyber.

```
GET https://connect.mindcloud.co/v1/universal/satoriCyber/latest/actions/search-authorization-analytics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Satori Cyber `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/satoriCyber/latest/actions/search-authorization-analytics?connectionId=$CONNECTION_ID&accountId=acc_12345" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "acc_12345"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/satoriCyber/latest/actions/search-authorization-analytics?${params}`, {
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
| `accountId` | string | yes | Satori account ID. Example: `acc_12345`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "dataStoreMaps": {},
      "nextPageToken": "string",
      "records": [
        {}
      ],
      "scopeMaps": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `dataStoreMaps` | object |  |
| `nextPageToken` | string |  |
| `records` | array<object> |  |
| `scopeMaps` | object |  |

## Native endpoint

Through the native Satori Cyber API, this operation is `GET /api/v1/authorization-analytics/:accountId/query` (base URL `https://app.satoricyber.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-authorization-analytics.md) for the provider-specific parameters and requirements.

