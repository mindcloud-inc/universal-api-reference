# Twenty: List Object Metadata



```
GET https://connect.mindcloud.co/v1/universal/twenty/latest/actions/list-object-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twenty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twenty/latest/actions/list-object-metadata?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twenty/latest/actions/list-object-metadata?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "fields": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "description": "string",
          "icon": "string",
          "id": "string",
          "isActive": true,
          "isCustom": true,
          "isNullable": true,
          "isSystem": true,
          "label": "string",
          "name": "Ava Chen",
          "type": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ],
      "icon": "string",
      "id": "string",
      "imageIdentifierFieldMetadataId": "string",
      "isActive": true,
      "isCustom": true,
      "isSystem": true,
      "labelIdentifierFieldMetadataId": "string",
      "labelPlural": "string",
      "labelSingular": "string",
      "namePlural": "Ava Chen",
      "nameSingular": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `description` | string |  |
| `fields[].createdAt` | date |  |
| `fields[].description` | string |  |
| `fields[].icon` | string |  |
| `fields[].id` | string |  |
| `fields[].isActive` | boolean |  |
| `fields[].isCustom` | boolean |  |
| `fields[].isNullable` | boolean |  |
| `fields[].isSystem` | boolean |  |
| `fields[].label` | string |  |
| `fields[].name` | string |  |
| `fields[].type` | string |  |
| `fields[].updatedAt` | date |  |
| `icon` | string |  |
| `id` | string |  |
| `imageIdentifierFieldMetadataId` | string |  |
| `isActive` | boolean |  |
| `isCustom` | boolean |  |
| `isSystem` | boolean |  |
| `labelIdentifierFieldMetadataId` | string |  |
| `labelPlural` | string |  |
| `labelSingular` | string |  |
| `namePlural` | string |  |
| `nameSingular` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Twenty API, this operation is `GET /rest/metadata/objects` (base URL `https://api.twenty.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-object-metadata.md) for the provider-specific parameters and requirements.

