# Cloudinary: Get Usage

Retrieves account usage details from Cloudinary.

```
GET https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/get-usage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudinary `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/get-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/get-usage?${params}`, {
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
      "bandwidth": {},
      "credits": {},
      "date_requested": "string",
      "derived_resources": 1,
      "impressions": {},
      "last_updated": "string",
      "media_limits": {},
      "objects": {},
      "plan": "string",
      "requests": 1,
      "resources": 1,
      "seconds_delivered": {},
      "storage": {},
      "transformations": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bandwidth` | object | Bandwidth usage summary. |
| `credits` | object | Credit usage summary. |
| `date_requested` | string | Date requested for usage metrics. |
| `derived_resources` | number | Number of derived resources. |
| `impressions` | object | Impression usage summary. |
| `last_updated` | string | Date when usage metrics were last updated. |
| `media_limits` | object | Media size and pixel limits. |
| `objects` | object | Object usage summary. |
| `plan` | string | Cloudinary account plan. |
| `requests` | number | Number of API requests. |
| `resources` | number | Number of primary resources. |
| `seconds_delivered` | object | Video delivery seconds usage summary. |
| `storage` | object | Storage usage summary. |
| `transformations` | object | Transformation usage summary. |

## Native endpoint

Through the native Cloudinary API, this operation is `GET /usage` (base URL `https://api.cloudinary.com/v1_1/{{credentials.cloudName}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-usage.md) for the provider-specific parameters and requirements.

