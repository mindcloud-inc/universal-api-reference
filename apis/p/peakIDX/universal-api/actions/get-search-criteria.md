# PeakIDX: Get Search Criteria

Retrieves configured search criteria from PeakIDX.

```
GET https://connect.mindcloud.co/v1/universal/peakIDX/latest/actions/get-search-criteria
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PeakIDX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/peakIDX/latest/actions/get-search-criteria?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/peakIDX/latest/actions/get-search-criteria?${params}`, {
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
      "acreage": [
        [
          {}
        ]
      ],
      "bathrooms": [
        [
          {}
        ]
      ],
      "bedrooms": [
        [
          {}
        ]
      ],
      "listStatus": [
        [
          {}
        ]
      ],
      "price": [
        [
          {}
        ]
      ],
      "sort": [
        [
          {}
        ]
      ],
      "sqft": [
        [
          {}
        ]
      ],
      "status": [
        [
          {}
        ]
      ],
      "type": [
        [
          {}
        ]
      ],
      "yearBuilt": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acreage[]` | array<object> | Available acreage filters. |
| `bathrooms[]` | array<object> | Available bathroom filter options. |
| `bathrooms[].label` | string | Displayed bathroom option label. |
| `bathrooms[].value` | string | Bathroom option value. |
| `bedrooms[]` | array<object> | Available bedroom filter options. |
| `bedrooms[].label` | string | Displayed bedroom option label. |
| `bedrooms[].value` | string | Bedroom option value. |
| `listStatus[]` | array<object> | Available listing status values. |
| `price[]` | array<object> | Available price filters. |
| `sort[]` | array<object> | Available sort options. |
| `sort[].label` | string | Sort option label. |
| `sort[].value` | string | Sort option value. |
| `sqft[]` | array<object> | Available square-footage filters. |
| `status[]` | array<object> | Available status values. |
| `type[]` | array<object> | Available property types. |
| `yearBuilt[]` | array<object> | Available year-built filters. |

## Native endpoint

Through the native PeakIDX API, this operation is `GET https://{{credentials.siteName}}.peakidxsites.com/search-criteria/` (base URL `https://account.peakidxsites.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-search-criteria.md) for the provider-specific parameters and requirements.

