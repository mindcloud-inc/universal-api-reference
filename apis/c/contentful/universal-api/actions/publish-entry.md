# Contentful: Publish entry



```
PUT https://connect.mindcloud.co/v1/universal/contentful/latest/actions/publish-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Contentful `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/contentful/latest/actions/publish-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/contentful/latest/actions/publish-entry', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `entryId` | string | no |  |
| `environmentId` | string | no |  |
| `spaceId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "metadata": {
        "tags": [
          {
            "sys": {
              "id": "string"
            }
          }
        ]
      },
      "sys": {
        "firstPublishedAt": "2026-05-07T12:00:00.000Z",
        "publishedAt": "2026-05-07T12:00:00.000Z",
        "publishedCounter": 1,
        "publishedVersion": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `metadata.tags[].sys.id` | string |  |
| `sys.firstPublishedAt` | date |  |
| `sys.publishedAt` | date |  |
| `sys.publishedCounter` | number |  |
| `sys.publishedVersion` | number |  |

## Native endpoint

Through the native Contentful API, this operation is `PUT /spaces/:spaceId/environments/:environmentId/entries/:entryId/published` (base URL `https://api.contentful.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/publish-entry.md) for the provider-specific parameters and requirements.

