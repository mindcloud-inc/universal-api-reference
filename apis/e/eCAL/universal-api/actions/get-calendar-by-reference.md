# ECAL: Get Calendar By Reference

Retrieves a calendar from ECAL by reference.

```
GET https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/get-calendar-by-reference
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ECAL `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/get-calendar-by-reference?connectionId=$CONNECTION_ID&reference=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "reference": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eCAL/latest/actions/get-calendar-by-reference?${params}`, {
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
| `reference` | string | yes | ECAL calendar reference value. |

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

Through the native ECAL API, this operation is `GET /calendar/:reference` (base URL `https://api.ecal.com/apiv2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-calendar-by-reference.md) for the provider-specific parameters and requirements.

