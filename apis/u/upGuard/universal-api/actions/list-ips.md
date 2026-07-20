# UpGuard: List IPs

Retrieves IP addresses from your UpGuard account.

```
GET https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/list-ips
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UpGuard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/list-ips?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/list-ips?${params}`, {
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
| `sortBy` | string | no | The value to sort the IPs by. |
| `sortDesc` | boolean | no | Whether or not to sort the results in descending order. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ips": [
        {
          "asn": 1,
          "asName": "Ava Chen",
          "country": "string",
          "ip": "string",
          "owner": "string",
          "services": [
            "string"
          ],
          "sources": [
            "string"
          ]
        }
      ],
      "nextPageToken": "string",
      "totalResults": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ips[].asn` | number |  |
| `ips[].asName` | string |  |
| `ips[].country` | string |  |
| `ips[].ip` | string |  |
| `ips[].owner` | string |  |
| `ips[].services[]` | string |  |
| `ips[].sources[]` | string |  |
| `nextPageToken` | string |  |
| `totalResults` | number |  |

## Native endpoint

Through the native UpGuard API, this operation is `GET /ips` (base URL `https://cyber-risk.upguard.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-ips.md) for the provider-specific parameters and requirements.

