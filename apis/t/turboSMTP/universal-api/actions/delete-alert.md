# turboSMTP: Delete Alert

Deletes an existing alert from turboSMTP.

```
DELETE https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/delete-alert
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a turboSMTP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/delete-alert?connectionId=$CONNECTION_ID&Id=9228" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "Id": "9228"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/delete-alert?${params}`, {
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
| `Id` | number | yes | Alert identifier. Example: `9228`. |

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
| `message` | string |  |

## Native endpoint

Through the native turboSMTP API, this operation is `DELETE /tools/alerts/{Id}` (base URL `https://pro.api.serversmtp.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-alert.md) for the provider-specific parameters and requirements.

