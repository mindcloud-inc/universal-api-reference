# Google Analytics: List Properties



```
GET https://connect.mindcloud.co/v1/universal/googleAnalytics/latest/actions/list-properties
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleAnalytics/latest/actions/list-properties?connectionId=$CONNECTION_ID&filter=parent%3Aaccounts%2F123456789" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filter": "parent:accounts/123456789"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleAnalytics/latest/actions/list-properties?${params}`, {
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
| `filter` | string | yes | Required Admin API filter, for example parent:accounts/123456789 Example: `parent:accounts/123456789`. |
| `pageSize` | number | no | Default: `50`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pageToken` | string | no |  |
| `showDeleted` | boolean | no | Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nextPageToken": "string",
      "properties": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nextPageToken` | string |  |
| `properties` | array<object> | Google Analytics properties matching the filter |

## Native endpoint

Through the native Google Analytics API, this operation is `GET https://analyticsadmin.googleapis.com/v1beta/properties` (base URL `https://analyticsdata.googleapis.com/v1beta`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-properties.md) for the provider-specific parameters and requirements.

