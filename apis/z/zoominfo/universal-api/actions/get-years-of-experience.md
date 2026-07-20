# Zoominfo: Get Years Of Experience

Retrieves years of experience values from ZoomInfo.

```
GET https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/get-years-of-experience
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoominfo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/get-years-of-experience?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zoominfo/latest/actions/get-years-of-experience?${params}`, {
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
      "yearsOfExperience": [
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
| `yearsOfExperience` | array<string> |  |

## Native endpoint

Through the native Zoominfo API, this operation is `GET lookup/years-of-experience` (base URL `https://api.zoominfo.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-years-of-experience.md) for the provider-specific parameters and requirements.

