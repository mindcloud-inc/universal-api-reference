# Calibre: Create Page Test

Creates a new page test in Calibre.

```
POST https://connect.mindcloud.co/v1/universal/calibre/latest/actions/create-page-test
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calibre `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/calibre/latest/actions/create-page-test" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.url": "https://example.com/",
  "variables.location": "SaoPaulo"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/calibre/latest/actions/create-page-test', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.url": "https://example.com/",
    "variables.location": "SaoPaulo"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.url` | string | yes | Example: `https://example.com/`. |
| `variables.location` | string | yes | Default: `SaoPaulo`. |
| `variables.device` | string | no | Default: `Desktop`. |
| `variables.connection` | string | no | Default: `cable`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.adBlockerIsEnabled` | boolean | no |  |
| `variables.isPrivate` | boolean | no |  |
| `variables.expiresAt` | date | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createTest": {
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
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createTest.adBlockerIsEnabled` | boolean |  |
| `createTest.connection.tag` | string |  |
| `createTest.connection.title` | string |  |
| `createTest.createdAt` | date |  |
| `createTest.device.tag` | string |  |
| `createTest.device.title` | string |  |
| `createTest.formattedTestUrl` | string |  |
| `createTest.isPrivate` | boolean |  |
| `createTest.location.shortName` | string |  |
| `createTest.location.tag` | string |  |
| `createTest.status` | string |  |
| `createTest.updatedAt` | date |  |
| `createTest.url` | string |  |
| `createTest.uuid` | string |  |

## Native endpoint

Through the native Calibre API, this operation is `POST /graphql` (base URL `https://api.calibreapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-page-test.md) for the provider-specific parameters and requirements.

