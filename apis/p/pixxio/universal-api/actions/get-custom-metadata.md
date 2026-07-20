# pixx.io: Get Custom Metadata

Retrieves a custom metadata field from your pixx.io workspace.

```
GET https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/get-custom-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a pixx.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/get-custom-metadata?connectionId=$CONNECTION_ID&customMetadataId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customMetadataId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/get-custom-metadata?${params}`, {
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
| `customMetadataId` | number | yes | The custom metadata ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customMetadata": {
        "id": 1,
        "name": "Ava Chen"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customMetadata` | object |  |
| `customMetadata.id` | number |  |
| `customMetadata.name` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native pixx.io API, this operation is `GET /metadata/custom/:custom_metadata_id` (base URL `https://mindcloudpixx260413.px.media/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-custom-metadata.md) for the provider-specific parameters and requirements.

