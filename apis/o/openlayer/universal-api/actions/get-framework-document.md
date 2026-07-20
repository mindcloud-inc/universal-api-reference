# Openlayer: Get Framework Document

Retrieves a framework document from Openlayer.

```
GET https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/get-framework-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Openlayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/get-framework-document?connectionId=$CONNECTION_ID&documentId=da4167ff-74fc-4857-8850-c496bc8de1a9&frameworkId=29e72db4-dd2f-4331-b1c4-d13b5160a404" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "da4167ff-74fc-4857-8850-c496bc8de1a9",
  "frameworkId": "29e72db4-dd2f-4331-b1c4-d13b5160a404"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openlayer/latest/actions/get-framework-document?${params}`, {
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
| `documentId` | string | yes | Openlayer framework document ID. Default: `da4167ff-74fc-4857-8850-c496bc8de1a9`. |
| `frameworkId` | string | yes | Openlayer framework ID. Default: `29e72db4-dd2f-4331-b1c4-d13b5160a404`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dateCreated": "string",
      "dateUpdated": "string",
      "frameworkId": "string",
      "id": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateCreated` | string |  |
| `dateUpdated` | string |  |
| `frameworkId` | string |  |
| `id` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Openlayer API, this operation is `GET /frameworks/:frameworkId/documents/:documentId` (base URL `https://api.openlayer.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-framework-document.md) for the provider-specific parameters and requirements.

