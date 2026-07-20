# Time Doctor: Get Tag

Retrieves a tag from Time Doctor.

```
GET https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/get-tag
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Time Doctor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/get-tag?connectionId=$CONNECTION_ID&tagId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tagId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/get-tag?${params}`, {
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
| `tagId` | string | yes | Unique identifier of the user group (tag). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creatorId": "string",
      "deleted": true,
      "id": "string",
      "managers": [
        "string"
      ],
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "readOnly": true,
      "ssoEnforcement": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `creatorId` | string |  |
| `deleted` | boolean |  |
| `id` | string |  |
| `managers` | array<string> |  |
| `modifiedAt` | date |  |
| `name` | string |  |
| `readOnly` | boolean |  |
| `ssoEnforcement` | object |  |

## Native endpoint

Through the native Time Doctor API, this operation is `GET /api/1.0/tags/:tagId` (base URL `https://api2.timedoctor.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tag.md) for the provider-specific parameters and requirements.

