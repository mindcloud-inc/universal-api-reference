# Geocodio: Delete Distance Job

Deletes an asynchronous distance job from Geocodio.

```
DELETE https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/delete-distance-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Geocodio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/delete-distance-job?connectionId=$CONNECTION_ID&identifier=abc123xyz" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "identifier": "abc123xyz"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/geocodio/latest/actions/delete-distance-job?${params}`, {
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
| `identifier` | string | yes | Distance job identifier. Example: `abc123xyz`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Deletion result message. |

## Native endpoint

Through the native Geocodio API, this operation is `DELETE /distance-jobs/{identifier}` (base URL `https://api.geocod.io/v1.12`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-distance-job.md) for the provider-specific parameters and requirements.

