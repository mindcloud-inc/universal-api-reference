# SearchApi: Get Map Place



```
GET https://connect.mindcloud.co/v1/universal/searchApi/latest/actions/get-map-place
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SearchApi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/searchApi/latest/actions/get-map-place?connectionId=$CONNECTION_ID&placeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "placeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/searchApi/latest/actions/get-map-place?${params}`, {
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
| `placeId` | string | yes | Google Maps place ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "admissions": [
        {}
      ],
      "atThisPlace": {},
      "experiences": [
        {}
      ],
      "peopleAlsoSearchFor": [
        {}
      ],
      "placeResult": {},
      "searchMetadata": {},
      "searchParameters": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `admissions` | array<object> |  |
| `atThisPlace` | object |  |
| `experiences` | array<object> |  |
| `peopleAlsoSearchFor` | array<object> |  |
| `placeResult` | object |  |
| `searchMetadata` | object |  |
| `searchParameters` | object |  |

## Native endpoint

Through the native SearchApi API, this operation is `GET /search` (base URL `https://www.searchapi.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-map-place.md) for the provider-specific parameters and requirements.

