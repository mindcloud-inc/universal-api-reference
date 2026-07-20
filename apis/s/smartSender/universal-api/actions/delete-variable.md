# Smart Sender: Delete Variable

Deletes an existing variable from Smart Sender.

```
DELETE https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/delete-variable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smart Sender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/delete-variable?connectionId=$CONNECTION_ID&variableId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variableId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/delete-variable?${params}`, {
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
| `variableId` | string | yes | The Smart Sender variable ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "state": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `state` | boolean |  |

## Native endpoint

Through the native Smart Sender API, this operation is `DELETE /v1/variables/:variableId` (base URL `https://api.smartsender.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-variable.md) for the provider-specific parameters and requirements.

