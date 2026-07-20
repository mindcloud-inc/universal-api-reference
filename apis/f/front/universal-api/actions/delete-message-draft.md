# Front: Delete Message Draft

Deletes an existing message draft from Front.

```
DELETE https://connect.mindcloud.co/v1/universal/front/latest/actions/delete-message-draft
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Front `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/front/latest/actions/delete-message-draft?connectionId=$CONNECTION_ID&draftId=msg_123&version=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "draftId": "msg_123",
  "version": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/front/latest/actions/delete-message-draft?${params}`, {
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
| `draftId` | string | yes | The draft ID. Example: `msg_123`. |
| `version` | string | yes | Version of the draft. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | The raw response body. The saved successful response was an empty string (HTTP 204). |

## Native endpoint

Through the native Front API, this operation is `DELETE /drafts/:draft_id` (base URL `https://api2.frontapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-message-draft.md) for the provider-specific parameters and requirements.

