# NiftyImages: Delete Map Location By Nifty ID

Deletes a map location from NiftyImages by Nifty ID.

```
DELETE https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/delete-map-location-by-nifty-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NiftyImages `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/delete-map-location-by-nifty-id?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com&niftyID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com",
  "niftyID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/niftyImages/latest/actions/delete-map-location-by-nifty-id?${params}`, {
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
| `niftyID` | string | yes | NiftyImages location ID to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native NiftyImages API returns.

## Native endpoint

Through the native NiftyImages API, this operation is `DELETE /Maps/DeleteLocation` (base URL `https://api.niftyimages.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-map-location-by-nifty-id.md) for the provider-specific parameters and requirements.

