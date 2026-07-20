# FogBugz: List Filters

Retrieves filters from FogBugz.

```
GET https://connect.mindcloud.co/v1/universal/fogBugz/latest/actions/list-filters
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FogBugz `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fogBugz/latest/actions/list-filters?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fogBugz/latest/actions/list-filters?${params}`, {
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
      "data": {
        "filters": [
          "string"
        ],
        "sFilter": "string",
        "type": "string"
      },
      "errorCode": {},
      "maxCacheAge": {},
      "meta": {
        "clientVersionAllowed": {
          "max": 1,
          "min": 1
        },
        "jsdbInvalidator": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.filters[]` | string |  |
| `data.sFilter` | string |  |
| `data.type` | string |  |
| `errorCode` | object |  |
| `maxCacheAge` | object |  |
| `meta.clientVersionAllowed.max` | number |  |
| `meta.clientVersionAllowed.min` | number |  |
| `meta.jsdbInvalidator` | string |  |

## Native endpoint

Through the native FogBugz API, this operation is `POST /listFilters` (base URL `{{credentials.siteUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-filters.md) for the provider-specific parameters and requirements.

