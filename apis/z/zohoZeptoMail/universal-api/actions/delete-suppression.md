# Zoho ZeptoMail: Delete Suppression

Deletes a suppression list entry from Zoho ZeptoMail.

```
DELETE https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/delete-suppression
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho ZeptoMail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/delete-suppression?connectionId=$CONNECTION_ID&type=string&values%5B0%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "type": "string",
  "values[0]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoZeptoMail/latest/actions/delete-suppression?${params}`, {
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
| `type` | string | yes | Suppression category to manage. |
| `values[0]` | string | yes | Email address or domain to remove from suppression. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "value": "string"
      },
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
| `data.value` | string |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho ZeptoMail API, this operation is `DELETE suppressions/:type` (base URL `https://api.zeptomail.com/v1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-suppression.md) for the provider-specific parameters and requirements.

