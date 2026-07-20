# Pipedrive: Get Person

Retrieves a person from Pipedrive.

```
GET https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/get-person
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/get-person?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/get-person?${params}`, {
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
| `id` | number | yes | Unique ID of the person. |
| `includeFields` | string | no | Comma-separated additional fields to include. |
| `customFields` | string | no | Comma-separated custom field keys to include. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addTime": "string",
      "customFields": {},
      "firstName": "Ava",
      "id": 1,
      "isDeleted": true,
      "lastName": "Chen",
      "name": "Ava Chen",
      "orgId": 1,
      "ownerId": 1,
      "pictureId": {},
      "updateTime": "string",
      "visibleTo": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addTime` | string |  |
| `customFields` | object |  |
| `firstName` | string |  |
| `id` | number |  |
| `isDeleted` | boolean |  |
| `lastName` | string |  |
| `name` | string |  |
| `orgId` | number |  |
| `ownerId` | number |  |
| `pictureId` | object |  |
| `updateTime` | string |  |
| `visibleTo` | number |  |

## Native endpoint

Through the native Pipedrive API, this operation is `GET v2/persons/:id` (base URL `{{credentials.accessTokenRequest.api_domain}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-person.md) for the provider-specific parameters and requirements.

