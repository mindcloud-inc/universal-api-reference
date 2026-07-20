# HubSpot: List Associations

Retrieves associations for a HubSpot record.

```
GET https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/list-associations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/list-associations?connectionId=$CONNECTION_ID&limit=25&offset=0&fromObject=string&objectId=string&toObjectType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "fromObject": "string",
  "objectId": "string",
  "toObjectType": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/list-associations?${params}`, {
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
| `fromObject` | string | yes | The source object type. |
| `objectId` | string | yes | The source record ID. |
| `toObjectType` | string | yes | The associated target object type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "associationTypes": [
        {}
      ],
      "toObjectId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `associationTypes` | array<object> | The association type details returned by HubSpot. |
| `toObjectId` | number | The associated record ID. |

## Native endpoint

Through the native HubSpot API, this operation is `GET crm/v4/objects/:fromObject/:objectId/associations/:toObjectType` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-associations.md) for the provider-specific parameters and requirements.

