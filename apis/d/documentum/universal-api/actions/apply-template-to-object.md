# Documentum: Apply Template To Object



```
PUT https://connect.mindcloud.co/v1/universal/documentum/latest/actions/apply-template-to-object
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documentum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/documentum/latest/actions/apply-template-to-object" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "repositoryName": "d2repo",
  "objectId": "090000018000abcd",
  "properties": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/documentum/latest/actions/apply-template-to-object', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "repositoryName": "d2repo",
    "objectId": "090000018000abcd",
    "properties": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `repositoryName` | string | yes | Documentum repository name. Example: `d2repo`. |
| `objectId` | string | yes | Documentum object ID to update with a template. Example: `090000018000abcd`. |
| `properties` | object | yes | JSON properties payload, for example template_name and folder_id. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "links": [
        {
          "href": "https://example.com",
          "rel": "https://example.com"
        }
      ],
      "properties": {
        "objectId": "string",
        "objectName": "Ava Chen"
      },
      "title": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Document identifier. |
| `links[].href` | string | Document link URL. |
| `links[].rel` | string | Document link relation. |
| `properties.objectId` | string | Document object identifier. |
| `properties.objectName` | string | Document object name. |
| `title` | string | Document title. |
| `updated` | date | Last update timestamp. |

## Native endpoint

Through the native Documentum API, this operation is `POST /repositories/{repositoryName}/objects-d2/{objectId}` (base URL `{{credentials.documentumRestBaseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/apply-template-to-object.md) for the provider-specific parameters and requirements.

