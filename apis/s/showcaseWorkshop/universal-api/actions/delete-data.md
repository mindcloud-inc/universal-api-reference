# Showcase Workshop: Delete Data

Deletes a data item from Showcase Workshop.

```
DELETE https://connect.mindcloud.co/v1/universal/showcaseWorkshop/latest/actions/delete-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Showcase Workshop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/showcaseWorkshop/latest/actions/delete-data?connectionId=$CONNECTION_ID&guid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "guid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/showcaseWorkshop/latest/actions/delete-data?${params}`, {
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
| `guid` | string | yes | Unique GUID of the data item to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | True when the delete request completed. |

## Native endpoint

Through the native Showcase Workshop API, this operation is `DELETE /data/{guid}` (base URL `https://app.showcaseworkshop.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-data.md) for the provider-specific parameters and requirements.

