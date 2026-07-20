# HubSpot: Get Listing By ID

Retrieves a listing from HubSpot by ID.

```
GET https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/get-listing-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/get-listing-by-id?connectionId=$CONNECTION_ID&objectTypeId=string&objectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "objectTypeId": "string",
  "objectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/get-listing-by-id?${params}`, {
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
| `objectTypeId` | string | yes | The Object Type ID. |
| `objectId` | string | yes |  |
| `properties[]` | array<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "properties": {},
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean | Whether the contact is archived. |
| `createdAt` | date | When the contact was created. |
| `id` | string | The contact record ID. |
| `properties` | object | The returned contact properties. |
| `updatedAt` | date | When the contact was last updated. |
| `url` | string | The HubSpot record URL. |

## Native endpoint

Through the native HubSpot API, this operation is `GET crm/objects/2026-03/:objectTypeId/:objectId` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-listing-by-id.md) for the provider-specific parameters and requirements.

