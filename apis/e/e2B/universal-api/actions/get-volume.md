# E2B: Get Volume

Retrieves a team volume from E2B.

```
GET https://connect.mindcloud.co/v1/universal/e2B/latest/actions/get-volume
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a E2B `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/e2B/latest/actions/get-volume?connectionId=$CONNECTION_ID&volumeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "volumeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/e2B/latest/actions/get-volume?${params}`, {
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
| `volumeId` | string | yes | Identifier of the volume. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "name": "Ava Chen",
      "token": "string",
      "volumeID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string | Name of the volume. |
| `token` | string | Auth token for interacting with volume content. |
| `volumeID` | string | ID of the volume. |

## Native endpoint

Through the native E2B API, this operation is `GET /volumes/{volumeID}` (base URL `https://api.e2b.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-volume.md) for the provider-specific parameters and requirements.

