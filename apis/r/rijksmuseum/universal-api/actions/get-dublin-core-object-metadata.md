# Rijksmuseum: Get Dublin Core Object Metadata



```
GET https://connect.mindcloud.co/v1/universal/rijksmuseum/latest/actions/get-dublin-core-object-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rijksmuseum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rijksmuseum/latest/actions/get-dublin-core-object-metadata?connectionId=$CONNECTION_ID&metadataObjectId=200107928" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "metadataObjectId": "200107928"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rijksmuseum/latest/actions/get-dublin-core-object-metadata?${params}`, {
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
| `metadataObjectId` | string | yes | Numeric Rijksmuseum metadata object ID, such as 200107928 for The Night Watch. Default: `200107928`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "@context": {},
      "@id": "string",
      "@type": "string",
      "creator": {},
      "date": "string",
      "description": "string",
      "identifier": "string",
      "relation": {},
      "rights": {},
      "subject": [
        {}
      ],
      "title": "string",
      "type": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `@context` | object |  |
| `@id` | string |  |
| `@type` | string |  |
| `creator` | object |  |
| `date` | string |  |
| `description` | string |  |
| `identifier` | string |  |
| `relation` | object |  |
| `rights` | object |  |
| `subject` | array<object> |  |
| `title` | string |  |
| `type` | object |  |

## Native endpoint

Through the native Rijksmuseum API, this operation is `GET /{{metadataObjectId}}` (base URL `https://data.rijksmuseum.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-dublin-core-object-metadata.md) for the provider-specific parameters and requirements.

