# Aspose: Update Document Property

Updates a document property in a presentation in Aspose.

```
PUT https://connect.mindcloud.co/v1/universal/aspose/latest/actions/update-document-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspose `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/aspose/latest/actions/update-document-property" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "propertyName": "Ava Chen",
  "property": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aspose/latest/actions/update-document-property', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "propertyName": "Ava Chen",
    "property": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The presentation file name. |
| `propertyName` | string | yes | The document property name. |
| `property` | object | yes | The document property payload. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Aspose API returns.

## Native endpoint

Through the native Aspose API, this operation is `PUT /slides/:name/documentproperties/:propertyName` (base URL `https://api.aspose.cloud/v3.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-document-property.md) for the provider-specific parameters and requirements.

