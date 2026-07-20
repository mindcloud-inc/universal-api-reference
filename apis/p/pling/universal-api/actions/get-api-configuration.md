# Pling: Get API Configuration

Retrieves OCS API configuration details from Pling.

```
GET https://connect.mindcloud.co/v1/universal/pling/latest/actions/get-api-configuration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pling/latest/actions/get-api-configuration?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pling/latest/actions/get-api-configuration?${params}`, {
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
      "contact": "string",
      "host": "string",
      "ssl": true,
      "version": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact` | string | Provider contact address. |
| `host` | string | Provider API host. |
| `ssl` | boolean | Whether SSL is supported. |
| `version` | string | OCS API version reported by Pling. |
| `website` | string | Provider website URL. |

## Native endpoint

Through the native Pling API, this operation is `GET /config` (base URL `https://api.pling.com/ocs/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-configuration.md) for the provider-specific parameters and requirements.

