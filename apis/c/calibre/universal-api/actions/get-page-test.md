# Calibre: Get Page Test

Retrieves a page test by UUID from Calibre.

```
GET https://connect.mindcloud.co/v1/universal/calibre/latest/actions/get-page-test
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calibre `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calibre/latest/actions/get-page-test?connectionId=$CONNECTION_ID&variables.uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calibre/latest/actions/get-page-test?${params}`, {
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
| `variables.uuid` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "organisation": {
        "singlePageTest": {
          "adBlockerIsEnabled": true,
          "artifactURL": "https://example.com",
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
          "mediaURL": "https://example.com",
          "status": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z",
          "url": "https://example.com",
          "uuid": "string",
          "webhookUrl": "https://example.com"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `organisation.singlePageTest.adBlockerIsEnabled` | boolean |  |
| `organisation.singlePageTest.artifactURL` | string |  |
| `organisation.singlePageTest.connection.tag` | string |  |
| `organisation.singlePageTest.connection.title` | string |  |
| `organisation.singlePageTest.createdAt` | date |  |
| `organisation.singlePageTest.device.tag` | string |  |
| `organisation.singlePageTest.device.title` | string |  |
| `organisation.singlePageTest.formattedTestUrl` | string |  |
| `organisation.singlePageTest.isPrivate` | boolean |  |
| `organisation.singlePageTest.location.shortName` | string |  |
| `organisation.singlePageTest.location.tag` | string |  |
| `organisation.singlePageTest.mediaURL` | string |  |
| `organisation.singlePageTest.status` | string |  |
| `organisation.singlePageTest.updatedAt` | date |  |
| `organisation.singlePageTest.url` | string |  |
| `organisation.singlePageTest.uuid` | string |  |
| `organisation.singlePageTest.webhookUrl` | string |  |

## Native endpoint

Through the native Calibre API, this operation is `POST /graphql` (base URL `https://api.calibreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-page-test.md) for the provider-specific parameters and requirements.

