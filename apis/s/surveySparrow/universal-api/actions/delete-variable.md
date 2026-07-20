# SurveySparrow: Delete Variable

Deletes a survey variable from SurveySparrow.

```
DELETE https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/delete-variable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SurveySparrow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/delete-variable?connectionId=$CONNECTION_ID&variableId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variableId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/delete-variable?${params}`, {
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
| `variableId` | number | yes | Variable ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native SurveySparrow API, this operation is `DELETE /variables/{{variableId}}` (base URL `https://api.surveysparrow.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-variable.md) for the provider-specific parameters and requirements.

