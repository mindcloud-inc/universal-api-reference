# DitLead: Delete Mailbox



```
DELETE https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/delete-mailbox
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DitLead `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/delete-mailbox?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ditLead/latest/actions/delete-mailbox?${params}`, {
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
| `mailboxAddress` | string | no |  |
| `mailboxId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `success` | boolean |  |

## Native endpoint

Through the native DitLead API, this operation is `DELETE /v1/mailbox` (base URL `https://api.ditlead.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-mailbox.md) for the provider-specific parameters and requirements.

