# 2Smart Cloud: All references



```
GET https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/list-references
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Smart Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/list-references?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartCloud/latest/actions/list-references?${params}`, {
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
      "firmware_bases": [
        {}
      ],
      "firmware_build_statuses": [
        "string"
      ],
      "firmware_build_types": [
        "string"
      ],
      "mcu_types": [
        {}
      ],
      "product_statuses": [
        "string"
      ],
      "release_types": [
        "string"
      ],
      "timelines_intervals": [
        "string"
      ],
      "timelines_periods": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `firmware_bases` | array<object> |  |
| `firmware_build_statuses` | array<string> |  |
| `firmware_build_types` | array<string> |  |
| `mcu_types` | array<object> |  |
| `product_statuses` | array<string> |  |
| `release_types` | array<string> |  |
| `timelines_intervals` | array<string> |  |
| `timelines_periods` | array<string> |  |

## Native endpoint

Through the native 2Smart Cloud API, this operation is `GET /references` (base URL `https://cloud.2smart.com/robot/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-references.md) for the provider-specific parameters and requirements.

