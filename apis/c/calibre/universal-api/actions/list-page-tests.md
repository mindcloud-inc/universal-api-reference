# Calibre: List Page Tests

Retrieves page tests for a site from Calibre.

```
GET https://connect.mindcloud.co/v1/universal/calibre/latest/actions/list-page-tests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calibre `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calibre/latest/actions/list-page-tests?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calibre/latest/actions/list-page-tests?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "organisation": {
        "singlePageTests": [
          {
            "adBlockerIsEnabled": true,
            "connection": {
              "tag": "string",
              "title": "string"
            },
            "createdAt": "2026-05-07T12:00:00.000Z",
            "device": {
              "tag": "string",
              "title": "string"
            },
            "formattedTestUrl": "https://example.com",
            "isPrivate": true,
            "location": {
              "shortName": "Ava Chen",
              "tag": "string"
            },
            "status": "string",
            "updatedAt": "2026-05-07T12:00:00.000Z",
            "url": "https://example.com",
            "uuid": "string"
          }
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `organisation.singlePageTests[].adBlockerIsEnabled` | boolean |  |
| `organisation.singlePageTests[].connection.tag` | string |  |
| `organisation.singlePageTests[].connection.title` | string |  |
| `organisation.singlePageTests[].createdAt` | date |  |
| `organisation.singlePageTests[].device.tag` | string |  |
| `organisation.singlePageTests[].device.title` | string |  |
| `organisation.singlePageTests[].formattedTestUrl` | string |  |
| `organisation.singlePageTests[].isPrivate` | boolean |  |
| `organisation.singlePageTests[].location.shortName` | string |  |
| `organisation.singlePageTests[].location.tag` | string |  |
| `organisation.singlePageTests[].status` | string |  |
| `organisation.singlePageTests[].updatedAt` | date |  |
| `organisation.singlePageTests[].url` | string |  |
| `organisation.singlePageTests[].uuid` | string |  |

## Native endpoint

Through the native Calibre API, this operation is `POST /graphql` (base URL `https://api.calibreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-page-tests.md) for the provider-specific parameters and requirements.

