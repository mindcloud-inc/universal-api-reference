# Addressfinder: Get AU Location Metadata

Retrieves metadata for an Australian location from Addressfinder.

```
GET https://connect.mindcloud.co/v1/universal/addressfinder/latest/actions/get-au-location-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Addressfinder `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/addressfinder/latest/actions/get-au-location-metadata?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/addressfinder/latest/actions/get-au-location-metadata?${params}`, {
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
| `id` | string | yes | Unique location identifier obtained from the AU Location Autocomplete API. |
| `domain` | string | no | Registered domain used for activity monitoring. |
| `format` | string | no | Response format. Default: `json`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Addressfinder API returns.

## Native endpoint

Through the native Addressfinder API, this operation is `GET /au/location/metadata` (base URL `https://api.addressfinder.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-au-location-metadata.md) for the provider-specific parameters and requirements.

