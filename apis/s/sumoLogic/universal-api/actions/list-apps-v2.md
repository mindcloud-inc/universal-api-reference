# Sumo Logic: List Apps V2

Retrieves apps from the Sumo Logic App Catalog.

```
GET https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-apps-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumo Logic `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-apps-v2?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-apps-v2?${params}`, {
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
| `name` | string | no | Name of the app. |
| `author` | string | no | Author of the app. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountTypes": [
        "string"
      ],
      "attributes": "string",
      "author": "string",
      "beta": true,
      "description": "string",
      "icon": "string",
      "installable": true,
      "installs": 1,
      "latestVersion": "string",
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "showOnMarketplace": true,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountTypes[]` | string |  |
| `attributes` | string |  |
| `author` | string |  |
| `beta` | boolean |  |
| `description` | string |  |
| `icon` | string |  |
| `installable` | boolean |  |
| `installs` | number |  |
| `latestVersion` | string |  |
| `modifiedAt` | date |  |
| `name` | string |  |
| `showOnMarketplace` | boolean |  |
| `uuid` | string |  |

## Native endpoint

Through the native Sumo Logic API, this operation is `GET /v2/apps` (base URL `https://api.sumologic.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-apps-v2.md) for the provider-specific parameters and requirements.

