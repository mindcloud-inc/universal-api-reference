# Zubie: Delete Place

Deletes a place from Zubie.

```
DELETE https://connect.mindcloud.co/v1/universal/zubie/latest/actions/delete-place
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zubie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/zubie/latest/actions/delete-place?connectionId=$CONNECTION_ID&place_key=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "place_key": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zubie/latest/actions/delete-place?${params}`, {
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
| `place_key` | string | yes | Unique place key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "key": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean |  |
| `key` | string |  |

## Native endpoint

Through the native Zubie API, this operation is `DELETE /place/{place_key}` (base URL `https://api.zubiecar.com/api/v2/zinc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-place.md) for the provider-specific parameters and requirements.

