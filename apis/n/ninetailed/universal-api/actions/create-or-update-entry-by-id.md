# Ninetailed: Create Or Update Entry By ID



```
PUT https://connect.mindcloud.co/v1/universal/ninetailed/latest/actions/create-or-update-entry-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ninetailed `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ninetailed/latest/actions/create-or-update-entry-by-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "spaceId": "string",
  "environmentId": "string",
  "entryId": "string",
  "contentTypeId": "string",
  "fields": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ninetailed/latest/actions/create-or-update-entry-by-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "spaceId": "string",
    "environmentId": "string",
    "entryId": "string",
    "contentTypeId": "string",
    "fields": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `spaceId` | string | yes | Contentful space ID. |
| `environmentId` | string | yes | Contentful environment ID. |
| `entryId` | string | yes | Contentful entry ID. |
| `contentTypeId` | string | yes | Content type ID to send as X-Contentful-Content-Type when creating by ID. |
| `fields` | object | yes | Localized entry fields object. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contentfulVersion` | number | no | Current entry version to send as X-Contentful-Version when updating an existing entry. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fields": {},
      "metadata": {},
      "sys": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fields` | object |  |
| `metadata` | object |  |
| `sys` | object |  |

## Native endpoint

Through the native Ninetailed API, this operation is `PUT /spaces/:space_id/environments/:environment_id/entries/:entry_id` (base URL `https://api.contentful.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-entry-by-id.md) for the provider-specific parameters and requirements.

