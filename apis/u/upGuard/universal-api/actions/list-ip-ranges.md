# UpGuard: List IP Ranges

Retrieves IP ranges from your UpGuard account.

```
GET https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/list-ip-ranges
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UpGuard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/list-ip-ranges?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/list-ip-ranges?${params}`, {
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
| `labels` | string<string> | no | Filter result by the provided labels Accepts multiple values in one string, delimited by `,`. |
| `pageToken` | string | no | The page_token from a previous request, use this to get the next page of results. |
| `pageSize` | number | no | The number of results to return per page. Default: `1000`. |
| `sortBy` | string | no | The value to sort the IP ranges by. |
| `sortDesc` | boolean | no | Whether or not to sort the results in descending order. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "totalResults": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `totalResults` | number |  |

## Native endpoint

Through the native UpGuard API, this operation is `GET /ranges` (base URL `https://cyber-risk.upguard.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-ip-ranges.md) for the provider-specific parameters and requirements.

