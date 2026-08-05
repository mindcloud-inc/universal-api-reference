# Google Analytics: Get Property Metadata



```
GET https://connect.mindcloud.co/v1/universal/googleAnalytics/latest/actions/get-property-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleAnalytics/latest/actions/get-property-metadata?connectionId=$CONNECTION_ID&propertyId=123456789" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "propertyId": "123456789"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleAnalytics/latest/actions/get-property-metadata?${params}`, {
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
| `propertyId` | string | yes | GA4 property ID without the properties/ prefix Example: `123456789`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dimensions": [
        {}
      ],
      "metrics": [
        {}
      ],
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dimensions` | array<object> | Available standard and custom dimensions |
| `metrics` | array<object> | Available standard and custom metrics |
| `name` | string | Metadata resource name |

## Native endpoint

Through the native Google Analytics API, this operation is `GET https://analyticsdata.googleapis.com/v1beta/properties/:propertyId/metadata` (base URL `https://analyticsdata.googleapis.com/v1beta`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-property-metadata.md) for the provider-specific parameters and requirements.

