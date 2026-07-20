# AccuWeather: Get Radar And Satellite Imagery 1024

Retrieves 1024px radar and satellite imagery from AccuWeather.

```
GET https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/get-tropical-storm-images1024
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AccuWeather `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/get-tropical-storm-images1024?connectionId=$CONNECTION_ID&locationKey=349727&resolution=1024x1024" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "locationKey": "349727",
  "resolution": "1024x1024"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/accuWeather/latest/actions/get-tropical-storm-images1024?${params}`, {
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
| `locationKey` | string | yes | Required AccuWeather location key. Default: `349727`. |
| `resolution` | string | yes | Required image size. Default: `1024x1024`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Link": "https://example.com",
      "MobileLink": "https://example.com",
      "Radar": {},
      "Satellite": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Link` | string |  |
| `MobileLink` | string |  |
| `Radar` | object |  |
| `Satellite` | object |  |

## Native endpoint

Through the native AccuWeather API, this operation is `GET /imagery/v1/maps/radsat/:resolution/:locationKey` (base URL `https://dataservice.accuweather.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tropical-storm-images1024.md) for the provider-specific parameters and requirements.

