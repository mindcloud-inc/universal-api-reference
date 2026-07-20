# SquareSpace: Retrieve Basic Site Information

Retrieves basic site information from Squarespace.

```
GET https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/retrieve-basic-site-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SquareSpace `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/retrieve-basic-site-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/retrieve-basic-site-information?${params}`, {
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
      "currency": "string",
      "id": "string",
      "language": "string",
      "location": {},
      "measurementStandard": "string",
      "siteId": "string",
      "timeZone": "string",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string |  |
| `id` | string |  |
| `language` | string |  |
| `location` | object |  |
| `measurementStandard` | string |  |
| `siteId` | string |  |
| `timeZone` | string |  |
| `title` | string |  |
| `url` | string |  |

## Native endpoint

Through the native SquareSpace API, this operation is `GET /1.0/authorization/website` (base URL `https://api.squarespace.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-basic-site-information.md) for the provider-specific parameters and requirements.

