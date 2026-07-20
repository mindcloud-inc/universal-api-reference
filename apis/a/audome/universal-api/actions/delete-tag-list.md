# Audome: Delete Tag List

Deletes an existing tag list from Audome.

```
DELETE https://connect.mindcloud.co/v1/universal/audome/latest/actions/delete-tag-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Audome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/audome/latest/actions/delete-tag-list?connectionId=$CONNECTION_ID&taglistUuid=968fc9b0-2f72-11f1-b639-d9947e744b2d" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taglistUuid": "968fc9b0-2f72-11f1-b639-d9947e744b2d"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/audome/latest/actions/delete-tag-list?${params}`, {
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
| `taglistUuid` | string | yes | Numeric tag-list identifier. Example: `968fc9b0-2f72-11f1-b639-d9947e744b2d`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Audome API returns.

## Native endpoint

Through the native Audome API, this operation is `DELETE /tag-lists/:taglistUuid` (base URL `https://app.audome.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-tag-list.md) for the provider-specific parameters and requirements.

