# Dynamic Mockups: Get Mockup

Retrieves a mockup from Dynamic Mockups by UUID.

```
GET https://connect.mindcloud.co/v1/universal/dynamicMockups/latest/actions/get-mockup
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dynamic Mockups `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dynamicMockups/latest/actions/get-mockup?connectionId=$CONNECTION_ID&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dynamicMockups/latest/actions/get-mockup?${params}`, {
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
| `uuid` | string | yes | UUID of the mockup to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
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
        "uuid": "string"
      },
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
| `data.collections[].name` | string |  |
| `data.collections[].uuid` | string |  |
| `data.name` | string |  |
| `data.smartObjects[].name` | string |  |
| `data.smartObjects[].position.left` | number |  |
| `data.smartObjects[].position.top` | number |  |
| `data.smartObjects[].printAreaPresets[].name` | string |  |
| `data.smartObjects[].printAreaPresets[].position.left` | number |  |
| `data.smartObjects[].printAreaPresets[].position.top` | number |  |
| `data.smartObjects[].printAreaPresets[].size.height` | number |  |
| `data.smartObjects[].printAreaPresets[].size.width` | number |  |
| `data.smartObjects[].printAreaPresets[].uuid` | string |  |
| `data.smartObjects[].size.height` | number |  |
| `data.smartObjects[].size.width` | number |  |
| `data.smartObjects[].uuid` | string |  |
| `data.thumbnail` | string |  |
| `data.thumbnails[].url` | string |  |
| `data.thumbnails[].width` | number |  |
| `data.uuid` | string |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Dynamic Mockups API, this operation is `GET api/v1/mockup/:uuid` (base URL `https://app.dynamicmockups.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-mockup.md) for the provider-specific parameters and requirements.

