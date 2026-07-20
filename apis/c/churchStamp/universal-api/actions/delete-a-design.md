# ChurchStamp: Delete a Design

Deletes an existing design from ChurchStamp by design ID.

```
DELETE https://connect.mindcloud.co/v1/universal/churchStamp/latest/actions/delete-a-design
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChurchStamp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/churchStamp/latest/actions/delete-a-design?connectionId=$CONNECTION_ID&designId=1731529343422x700557600439664600" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "designId": "1731529343422x700557600439664600"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/churchStamp/latest/actions/delete-a-design?${params}`, {
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
| `designId` | string | yes | Unique identifier for the design to delete. Example: `1731529343422x700557600439664600`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native ChurchStamp API, this operation is `POST /delete-design` (base URL `https://v2.churchstamp.com/api/1.1/wf`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-a-design.md) for the provider-specific parameters and requirements.

