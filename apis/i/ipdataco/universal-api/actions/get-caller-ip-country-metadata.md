# ipdata.co: Get Caller IP Country Metadata



```
GET https://connect.mindcloud.co/v1/universal/ipdataco/latest/actions/get-caller-ip-country-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ipdata.co `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ipdataco/latest/actions/get-caller-ip-country-metadata?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ipdataco/latest/actions/get-caller-ip-country-metadata?${params}`, {
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
      "calling_code": "string",
      "continent_code": "string",
      "continent_name": "Ava Chen",
      "emoji_flag": "string",
      "emoji_unicode": "string",
      "flag": "string",
      "is_eu": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calling_code` | string |  |
| `continent_code` | string |  |
| `continent_name` | string |  |
| `emoji_flag` | string |  |
| `emoji_unicode` | string |  |
| `flag` | string |  |
| `is_eu` | boolean |  |

## Native endpoint

Through the native ipdata.co API, this operation is `GET /` (base URL `https://api.ipdata.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-caller-ip-country-metadata.md) for the provider-specific parameters and requirements.

