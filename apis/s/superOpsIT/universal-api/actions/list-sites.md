# SuperOps IT: List Sites



```
GET https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/list-sites
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperOps IT `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/list-sites?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/list-sites?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "getSiteList": {
        "listInfo": {
          "page": 1,
          "pageSize": 1,
          "totalCount": 1
        },
        "sites": [
          {
            "address": {
              "addressId": "string",
              "countryCode": "string"
            },
            "contactNumber": "string",
            "id": "string",
            "name": "Ava Chen",
            "timezoneCode": "string",
            "working24x7": true
          }
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `getSiteList.listInfo.page` | number |  |
| `getSiteList.listInfo.pageSize` | number |  |
| `getSiteList.listInfo.totalCount` | number |  |
| `getSiteList.sites[].address.addressId` | string |  |
| `getSiteList.sites[].address.countryCode` | string |  |
| `getSiteList.sites[].contactNumber` | string |  |
| `getSiteList.sites[].id` | string |  |
| `getSiteList.sites[].name` | string |  |
| `getSiteList.sites[].timezoneCode` | string |  |
| `getSiteList.sites[].working24x7` | boolean |  |

## Native endpoint

Through the native SuperOps IT API, this operation is `POST /it` (base URL `https://api.superops.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sites.md) for the provider-specific parameters and requirements.

