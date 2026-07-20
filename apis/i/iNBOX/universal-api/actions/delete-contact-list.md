# INBOX: Delete Contact List

Deletes an existing contact list from INBOX.

```
DELETE https://connect.mindcloud.co/v1/universal/iNBOX/latest/actions/delete-contact-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a INBOX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/iNBOX/latest/actions/delete-contact-list?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iNBOX/latest/actions/delete-contact-list?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "resultCode": 1,
      "resultMessage": "string",
      "resultObject": true,
      "resultStatus": true,
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `resultCode` | number |  |
| `resultMessage` | string |  |
| `resultObject` | boolean |  |
| `resultStatus` | boolean |  |
| `version` | string |  |

## Native endpoint

Through the native INBOX API, this operation is `DELETE /inbox/v1/contactlists/:id` (base URL `https://useapi.useinbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-contact-list.md) for the provider-specific parameters and requirements.

