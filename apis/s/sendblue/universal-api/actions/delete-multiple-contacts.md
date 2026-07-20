# Sendblue: Delete Multiple Contacts

Deletes multiple contacts from Sendblue.

```
DELETE https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/delete-multiple-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendblue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/delete-multiple-contacts?connectionId=$CONNECTION_ID&contactIds%5B%5D=%2B14155550123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactIds[]": "+14155550123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/delete-multiple-contacts?${params}`, {
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
| `contactIds[]` | array<string> | yes | Array of phone numbers in E.164 format to delete. Example: `+14155550123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "failures": 1,
      "results": [
        {
          "error": "string",
          "phoneNumber": "string",
          "success": true
        }
      ],
      "status": "string",
      "successes": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `failures` | number |  |
| `results[].error` | string |  |
| `results[].phoneNumber` | string |  |
| `results[].success` | boolean |  |
| `status` | string |  |
| `successes` | number |  |
| `total` | number |  |

## Native endpoint

Through the native Sendblue API, this operation is `DELETE /api/v2/contacts` (base URL `https://api.sendblue.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-multiple-contacts.md) for the provider-specific parameters and requirements.

