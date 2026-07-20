# ECAL: Get Calendar

Retrieves a calendar from ECAL by ID.

```
GET https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/get-calendar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ECAL `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/get-calendar?connectionId=$CONNECTION_ID&calendarId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "calendarId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/get-calendar?${params}`, {
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
| `calendarId` | string | yes | ECAL calendar ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "categoryIds": [
        "string"
      ],
      "feed": "string",
      "genre": "string",
      "id": "string",
      "latestVersion": 1,
      "name": "Ava Chen",
      "note": "string",
      "publisherId": 1,
      "publisherOrgId": 1,
      "reference": "string",
      "subGenre": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categoryIds` | array<string> |  |
| `feed` | string |  |
| `genre` | string |  |
| `id` | string |  |
| `latestVersion` | number |  |
| `name` | string |  |
| `note` | string |  |
| `publisherId` | number |  |
| `publisherOrgId` | number |  |
| `reference` | string |  |
| `subGenre` | string |  |

## Native endpoint

Through the native ECAL API, this operation is `GET /calendar/:calendarId` (base URL `https://api.ecal.com/apiv2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-calendar.md) for the provider-specific parameters and requirements.

