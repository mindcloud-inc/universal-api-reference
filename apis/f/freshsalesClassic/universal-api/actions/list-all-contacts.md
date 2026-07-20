# Freshsales Classic: List All Contacts

Retrieves contacts from a Freshsales Classic view.

```
GET https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/list-all-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshsales Classic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/list-all-contacts?connectionId=$CONNECTION_ID&viewId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "viewId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/list-all-contacts?${params}`, {
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
| `page` | number | no | Page number to return for the selected contact view. |
| `viewId` | number | yes | The contact view ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city": "string",
      "country": "string",
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "jobTitle": "string",
      "lastName": "Chen",
      "leadScore": 1,
      "mobileNumber": "string",
      "openDealsAmount": "string",
      "state": "string",
      "tags": [
        "string"
      ],
      "wonDealsAmount": "string",
      "workNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string |  |
| `country` | string |  |
| `displayName` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `jobTitle` | string |  |
| `lastName` | string |  |
| `leadScore` | number |  |
| `mobileNumber` | string |  |
| `openDealsAmount` | string |  |
| `state` | string |  |
| `tags` | array<string> |  |
| `wonDealsAmount` | string |  |
| `workNumber` | string |  |

## Native endpoint

Through the native Freshsales Classic API, this operation is `GET /contacts/view/:viewId` (base URL `https://{{credentials.bundleAlias}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-all-contacts.md) for the provider-specific parameters and requirements.

