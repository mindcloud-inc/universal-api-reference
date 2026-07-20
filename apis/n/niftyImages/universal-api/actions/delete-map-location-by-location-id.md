# NiftyImages: Delete Map Location By Location ID

Deletes a map location from NiftyImages by location ID.

```
DELETE https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/delete-map-location-by-location-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NiftyImages `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/delete-map-location-by-location-id?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com&locationID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com",
  "locationID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/delete-map-location-by-location-id?${params}`, {
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
| `url` | string | yes | NiftyImages map URL. |
| `locationID` | string | yes | Location ID to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native NiftyImages API returns.

## Native endpoint

Through the native NiftyImages API, this operation is `DELETE /Maps/DeleteLocation` (base URL `https://api.niftyimages.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-map-location-by-location-id.md) for the provider-specific parameters and requirements.

