# ECAL: List Calendars

Retrieves calendars from ECAL.

```
GET https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/list-calendars
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ECAL `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/list-calendars?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/list-calendars?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `showDraft` | boolean | no | Whether to include draft calendars. Default: `false`. |

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
| `categoryIds` | array<string> | Calendar category IDs. |
| `feed` | string | Calendar feed URL or identifier. |
| `genre` | string | Calendar genre. |
| `id` | string | ECAL calendar ID. |
| `latestVersion` | number | Latest calendar version. |
| `name` | string | Calendar name. |
| `note` | string | Calendar note. |
| `publisherId` | number | Publisher ID. |
| `publisherOrgId` | number | Publisher organization ID. |
| `reference` | string | Calendar reference value when present. |
| `subGenre` | string | Calendar sub-genre. |

## Native endpoint

Through the native ECAL API, this operation is `GET /calendar/` (base URL `https://api.ecal.com/apiv2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-calendars.md) for the provider-specific parameters and requirements.

