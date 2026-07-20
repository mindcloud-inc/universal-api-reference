# Swipe One: Get Contact Property



```
GET https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/get-contact-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Swipe One `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/get-contact-property?connectionId=$CONNECTION_ID&contactPropertyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactPropertyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/get-contact-property?${params}`, {
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
| `contactPropertyId` | string | yes | Contact property to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {},
      "dataType": "string",
      "fieldType": "string",
      "Id": "string",
      "isArchived": true,
      "isEnabled": true,
      "label": "string",
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `createdAt` | date |  |
| `createdBy` | object |  |
| `dataType` | string |  |
| `fieldType` | string |  |
| `Id` | string |  |
| `isArchived` | boolean |  |
| `isEnabled` | boolean |  |
| `label` | string |  |
| `name` | string |  |
| `updatedAt` | date |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Swipe One API, this operation is `GET /contact-properties/:contactPropertyId` (base URL `https://api.swipeone.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact-property.md) for the provider-specific parameters and requirements.

