# MailBluster: Delete Lead

Deletes an existing lead from MailBluster by lead hash.

```
DELETE https://connect.mindcloud.co/v1/universal/mailBluster/latest/actions/delete-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailBluster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/mailBluster/latest/actions/delete-lead?connectionId=$CONNECTION_ID&leadHash=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "leadHash": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailBluster/latest/actions/delete-lead?${params}`, {
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
| `leadHash` | string | yes | MD5 hash of the lead email to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "leadHash": "string",
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `leadHash` | string | MD5 hash of the deleted lead email. |
| `message` | string | Operation result message. |

## Native endpoint

Through the native MailBluster API, this operation is `DELETE /leads/:leadHash` (base URL `https://api.mailbluster.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-lead.md) for the provider-specific parameters and requirements.

