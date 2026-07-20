# Aspose: Delete Document Property

Deletes a document property from a presentation in Aspose.

```
DELETE https://connect.mindcloud.co/v1/universal/aspose/latest/actions/delete-document-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspose `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/aspose/latest/actions/delete-document-property?connectionId=$CONNECTION_ID&name=Ava%20Chen&propertyName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen",
  "propertyName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aspose/latest/actions/delete-document-property?${params}`, {
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
| `name` | string | yes | The presentation file name. |
| `propertyName` | string | yes | The document property name. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Aspose API returns.

## Native endpoint

Through the native Aspose API, this operation is `DELETE /slides/:name/documentproperties/:propertyName` (base URL `https://api.aspose.cloud/v3.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-document-property.md) for the provider-specific parameters and requirements.

