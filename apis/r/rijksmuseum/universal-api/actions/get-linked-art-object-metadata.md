# Rijksmuseum: Get Linked Art Object Metadata



```
GET https://connect.mindcloud.co/v1/universal/rijksmuseum/latest/actions/get-linked-art-object-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rijksmuseum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rijksmuseum/latest/actions/get-linked-art-object-metadata?connectionId=$CONNECTION_ID&metadataObjectId=200107928" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "metadataObjectId": "200107928"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rijksmuseum/latest/actions/get-linked-art-object-metadata?${params}`, {
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
      "@context": "string",
      "current_location": {},
      "id": "string",
      "identified_by": [
        {}
      ],
      "member_of": [
        {}
      ],
      "produced_by": {},
      "subject_of": [
        {}
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `@context` | string |  |
| `current_location` | object |  |
| `id` | string |  |
| `identified_by` | array<object> |  |
| `member_of` | array<object> |  |
| `produced_by` | object |  |
| `subject_of` | array<object> |  |
| `type` | string |  |

## Native endpoint

Through the native Rijksmuseum API, this operation is `GET /{{metadataObjectId}}` (base URL `https://data.rijksmuseum.nl`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-linked-art-object-metadata.md) for the provider-specific parameters and requirements.

