# GSA Public Comment: Get Docket

Retrieves a specific docket from GSA Public Comment.

```
GET https://connect.mindcloud.co/v1/universal/gSAPublicComment/latest/actions/get-docket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GSA Public Comment `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gSAPublicComment/latest/actions/get-docket?connectionId=$CONNECTION_ID&docketId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "docketId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gSAPublicComment/latest/actions/get-docket?${params}`, {
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
| `docketId` | string | yes | ID of the docket to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "attributes": {
          "agencyId": "string",
          "category": "string",
          "displayProperties": [
            {}
          ],
          "dkAbstract": "string",
          "docketType": "string",
          "modifyDate": "2026-05-07T12:00:00.000Z",
          "objectId": "string",
          "rin": "string",
          "subType": "string",
          "title": "string"
        },
        "id": "string",
        "links": {
          "self": "https://example.com"
        },
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Docket resource. |
| `data.attributes.agencyId` | string |  |
| `data.attributes.category` | string |  |
| `data.attributes.displayProperties` | array<object> |  |
| `data.attributes.dkAbstract` | string |  |
| `data.attributes.docketType` | string |  |
| `data.attributes.modifyDate` | date |  |
| `data.attributes.objectId` | string |  |
| `data.attributes.rin` | string |  |
| `data.attributes.subType` | string |  |
| `data.attributes.title` | string |  |
| `data.id` | string | Docket ID. |
| `data.links.self` | string |  |
| `data.type` | string |  |

## Native endpoint

Through the native GSA Public Comment API, this operation is `GET /dockets/:docketId` (base URL `https://api.regulations.gov/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-docket.md) for the provider-specific parameters and requirements.

