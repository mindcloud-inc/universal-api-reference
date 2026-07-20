# Ragic: Get Attachment / File

Retrieves an attachment or file from Ragic.

```
GET https://connect.mindcloud.co/v1/universal/ragic/latest/actions/get-attachment-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ragic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ragic/latest/actions/get-attachment-file?connectionId=$CONNECTION_ID&accountName=Ava%20Chen&fileName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountName": "Ava Chen",
  "fileName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ragic/latest/actions/get-attachment-file?${params}`, {
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
| `accountName` | string | yes | Ragic account name used in the download URL. |
| `fileName` | string | yes | Attachment token returned by Ragic record data, including the prefix before the @ symbol. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[]` | number |  |
| `type` | string |  |

## Native endpoint

Through the native Ragic API, this operation is `GET {{credentials.serverUrl}}/file.jsp` (base URL `{{credentials.serverUrl}}/mindcloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-attachment-file.md) for the provider-specific parameters and requirements.

