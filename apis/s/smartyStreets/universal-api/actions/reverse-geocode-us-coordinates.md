# Smarty-streets: Reverse Geocode US Coordinates

Finds nearby US addresses in Smarty-streets by latitude and longitude.

```
GET https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/reverse-geocode-us-coordinates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smarty-streets `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/reverse-geocode-us-coordinates?connectionId=$CONNECTION_ID&latitude=64.75214&longitude=-147.353" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "latitude": "64.75214",
  "longitude": "-147.353"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartyStreets/latest/actions/reverse-geocode-us-coordinates?${params}`, {
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
| `latitude` | number | yes | Latitude in decimal degrees. Default: `64.75214`. Example: `64.75214`. |
| `longitude` | number | yes | Longitude in decimal degrees. Default: `-147.353`. Example: `-147.353`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Smarty-streets API returns.

## Native endpoint

Through the native Smarty-streets API, this operation is `GET https://us-reverse-geo.api.smarty.com/lookup` (base URL `https://us-street.api.smarty.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reverse-geocode-us-coordinates.md) for the provider-specific parameters and requirements.

