# UseINBOX: Get Contact Import Status

Retrieves contact import status from UseINBOX.

```
GET https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/get-contact-import-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UseINBOX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/get-contact-import-status?connectionId=$CONNECTION_ID&contactListId=string&importId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactListId": "string",
  "importId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/useINBOX/latest/actions/get-contact-import-status?${params}`, {
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
| `contactListId` | string | yes | Contact list ID from INBOX. |
| `importId` | string | yes | Import job ID from INBOX. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "importedCount": 1,
      "status": "string",
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `importedCount` | number |  |
| `status` | string |  |
| `totalCount` | number |  |

## Native endpoint

Through the native UseINBOX API, this operation is `GET /inbox/v1/contactlists/:contactListId/import/:importId` (base URL `https://useapi.useinbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-import-status.md) for the provider-specific parameters and requirements.

