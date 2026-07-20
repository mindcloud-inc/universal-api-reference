# IntakeQ: Remove Client Tag

Deletes a client tag assignment from IntakeQ.

```
DELETE https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/remove-client-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IntakeQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/remove-client-tag?connectionId=$CONNECTION_ID&clientId=string&tag=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "clientId": "string",
  "tag": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/remove-client-tag?${params}`, {
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
| `clientId` | string | yes | The IntakeQ numeric client ID. |
| `tag` | string | yes | The client tag to remove. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientId": 1,
      "tag": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientId` | number |  |
| `tag` | string |  |

## Native endpoint

Through the native IntakeQ API, this operation is `DELETE /clientTags` (base URL `https://intakeq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-client-tag.md) for the provider-specific parameters and requirements.

