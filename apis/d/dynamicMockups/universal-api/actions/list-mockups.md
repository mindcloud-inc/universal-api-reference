# Dynamic Mockups: List Mockups

Retrieves your mockups from Dynamic Mockups.

```
GET https://connect.mindcloud.co/v1/universal/dynamicMockups/latest/actions/list-mockups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dynamic Mockups `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dynamicMockups/latest/actions/list-mockups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dynamicMockups/latest/actions/list-mockups?${params}`, {
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
| `include_all_catalogs` | boolean | no | Set true to include mockups across all catalogs. Example: `true \| false`. |
| `catalog_uuid` | string | no | Optional catalog UUID filter. Example: `e.g. b1d8fac5-b8d1-4af8-99d9-8c4155a0f24d`. |
| `collection_uuid` | string | no | Optional collection UUID filter. Example: `e.g. 0663101b-f01c-4e85-89af-f90b4e9f983b`. |
| `name` | string | no | Optional name filter. Example: `optional name filter`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "collections": [
            {
              "name": "Ava Chen",
              "uuid": "string"
            }
          ],
          "name": "Ava Chen",
          "smartObjects": [
            {
              "name": "Ava Chen",
              "position": {
                "left": 1,
                "top": 1
              },
              "printAreaPresets": [
                {
                  "name": "Ava Chen",
                  "position": {
                    "left": 1,
                    "top": 1
                  },
                  "size": {
                    "height": 1,
                    "width": 1
                  },
                  "uuid": "string"
                }
              ],
              "size": {
                "height": 1,
                "width": 1
              },
              "uuid": "string"
            }
          ],
          "thumbnail": "string",
          "thumbnails": [
            {
              "url": "https://example.com",
              "width": 1
            }
          ],
          "type": "string",
          "uuid": "string"
        }
      ],
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].collections[].name` | string |  |
| `data[].collections[].uuid` | string |  |
| `data[].name` | string |  |
| `data[].smartObjects[].name` | string |  |
| `data[].smartObjects[].position.left` | number |  |
| `data[].smartObjects[].position.top` | number |  |
| `data[].smartObjects[].printAreaPresets[].name` | string |  |
| `data[].smartObjects[].printAreaPresets[].position.left` | number |  |
| `data[].smartObjects[].printAreaPresets[].position.top` | number |  |
| `data[].smartObjects[].printAreaPresets[].size.height` | number |  |
| `data[].smartObjects[].printAreaPresets[].size.width` | number |  |
| `data[].smartObjects[].printAreaPresets[].uuid` | string |  |
| `data[].smartObjects[].size.height` | number |  |
| `data[].smartObjects[].size.width` | number |  |
| `data[].smartObjects[].uuid` | string |  |
| `data[].thumbnail` | string |  |
| `data[].thumbnails[].url` | string |  |
| `data[].thumbnails[].width` | number |  |
| `data[].type` | string |  |
| `data[].uuid` | string |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Dynamic Mockups API, this operation is `GET api/v1/mockups` (base URL `https://app.dynamicmockups.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-mockups.md) for the provider-specific parameters and requirements.

