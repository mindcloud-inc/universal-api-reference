# SigningHub: List Attachments

Retrieves attachments from SigningHub.

```
GET https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/list-attachments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SigningHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/list-attachments?connectionId=$CONNECTION_ID&documentId=1&packageId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "1",
  "packageId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/list-attachments?${params}`, {
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
| `documentId` | number | yes | Document ID of the document whose attachments are requested. |
| `packageId` | number | yes | Package ID of the package to which the document belongs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachment_id": 1,
      "attachment_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachment_id` | number |  |
| `attachment_name` | string |  |

## Native endpoint

Through the native SigningHub API, this operation is `GET /v4/packages/:packageId/documents/:documentId/attachments` (base URL `https://api.signinghub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-attachments.md) for the provider-specific parameters and requirements.

