# Airlabs: Delete Flight Alert Listener

Deletes a flight alert listener from Airlabs.

```
DELETE https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/delete-flight-alert-listener
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airlabs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/delete-flight-alert-listener?connectionId=$CONNECTION_ID&listenerId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listenerId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airlabs/latest/actions/delete-flight-alert-listener?${params}`, {
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
| `listenerId` | number | yes | ID of the previously created listener to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "unlistened": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `unlistened` | boolean | Whether the listener was removed. |

## Native endpoint

Through the native Airlabs API, this operation is `GET /unlisten` (base URL `https://airlabs.co/api/v9`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-flight-alert-listener.md) for the provider-specific parameters and requirements.

