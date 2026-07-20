# Sigma: List Connection Path Grants



```
GET https://connect.mindcloud.co/v1/universal/sigma/latest/actions/list-connection-path-grants
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sigma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sigma/latest/actions/list-connection-path-grants?connectionId=$CONNECTION_ID&connectionPathId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "connectionPathId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sigma/latest/actions/list-connection-path-grants?${params}`, {
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
| `connectionPathId` | string | yes | Sigma connectionPathId. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entries": [
        {}
      ],
      "hasMore": true,
      "nextPage": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entries` | array<object> | Connection path grant entries |
| `hasMore` | boolean | Deprecated pagination hint |
| `nextPage` | string | Cursor for the next page of grants |
| `total` | number | Total number of grants |

## Native endpoint

Through the native Sigma API, this operation is `GET /v2/connections/paths/{connectionPathId}/grants` (base URL `https://aws-api.sigmacomputing.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-connection-path-grants.md) for the provider-specific parameters and requirements.

