# Airzone Cloud: Get Installation Location

Retrieves an installation location from Airzone Cloud.

```
GET https://connect.mindcloud.co/v1/universal/airzoneCloud/latest/actions/get-installation-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airzone Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airzoneCloud/latest/actions/get-installation-location?connectionId=$CONNECTION_ID&locationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "locationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airzoneCloud/latest/actions/get-installation-location?${params}`, {
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
| `locationId` | string | yes | The Airzone location identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "coords": {},
      "google_place_id": "string",
      "text": {},
      "timezoneId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | Location ID. |
| `coords` | object | Location coordinates. |
| `google_place_id` | string | Google Place ID. |
| `text` | object | Localized city and country labels. |
| `timezoneId` | string | Location timezone identifier. |

## Native endpoint

Through the native Airzone Cloud API, this operation is `GET /installations/location/{locationId}` (base URL `https://m.airzonecloud.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-installation-location.md) for the provider-specific parameters and requirements.

