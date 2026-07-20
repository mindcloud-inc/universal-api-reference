# Webshipper: List Labels

Retrieves labels from Webshipper.

```
GET https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/list-labels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webshipper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/list-labels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/list-labels?${params}`, {
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
      "attributes": {
        "base64": "string",
        "createdAt": "string",
        "labelFormat": "string",
        "labelSize": "string",
        "shipmentId": 1,
        "updatedAt": "string"
      },
      "id": "string",
      "links": {
        "self": "https://example.com"
      },
      "meta": {
        "copyright": "string"
      },
      "relationships": {
        "printJobs": {
          "links": {
            "related": "https://example.com",
            "self": "https://example.com"
          }
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.base64` | string |  |
| `attributes.createdAt` | string |  |
| `attributes.labelFormat` | string |  |
| `attributes.labelSize` | string |  |
| `attributes.shipmentId` | number |  |
| `attributes.updatedAt` | string |  |
| `id` | string |  |
| `links.self` | string |  |
| `meta.copyright` | string |  |
| `relationships.printJobs.links.related` | string |  |
| `relationships.printJobs.links.self` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Webshipper API, this operation is `GET /labels` (base URL `https://{{credentials.accountName}}.api.webshipper.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-labels.md) for the provider-specific parameters and requirements.

