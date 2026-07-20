# Clearout: Delete Bulk Email Verification Result

Deletes a bulk email verification result from Clearout.

```
DELETE https://connect.mindcloud.co/v1/universal/clearout/latest/actions/delete-bulk-email-verification-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clearout `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/clearout/latest/actions/delete-bulk-email-verification-result?connectionId=$CONNECTION_ID&listId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clearout/latest/actions/delete-bulk-email-verification-result?${params}`, {
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
| `listId` | string | yes | Pass the value of bulk list_id property from response object |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ignoreResult` | boolean | no | Set this value to true when download request is in progress, otherwise list removal will be denied Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdOn": "string",
      "name": "Ava Chen",
      "source": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdOn` | string |  |
| `name` | string |  |
| `source` | string |  |

## Native endpoint

Through the native Clearout API, this operation is `POST /email_verify/list/remove` (base URL `https://api.clearout.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-bulk-email-verification-result.md) for the provider-specific parameters and requirements.

