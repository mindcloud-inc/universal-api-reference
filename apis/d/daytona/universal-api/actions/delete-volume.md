# Daytona: Delete Volume

Deletes an existing volume from Daytona.

```
DELETE https://connect.mindcloud.co/v1/universal/daytona/latest/actions/delete-volume
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Daytona `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/daytona/latest/actions/delete-volume?connectionId=$CONNECTION_ID&volumeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "volumeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/daytona/latest/actions/delete-volume?${params}`, {
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
| `volumeId` | string | yes | Volume ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Daytona API returns.

## Native endpoint

Through the native Daytona API, this operation is `DELETE /volumes/[:volumeId]` (base URL `https://app.daytona.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-volume.md) for the provider-specific parameters and requirements.

