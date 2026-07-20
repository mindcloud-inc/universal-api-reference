# RD Station Marketing: List Segmentation Contacts



```
GET https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/list-segmentation-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RD Station Marketing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/list-segmentation-contacts?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rDStationMarketing/latest/actions/list-segmentation-contacts?${params}`, {
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
| `id` | string | yes | Segmentation ID in path. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contacts": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "email": "ava@example.com",
          "lastConversionDate": "2026-05-07T12:00:00.000Z",
          "links": [
            {
              "href": "https://example.com"
            }
          ],
          "name": "Ava Chen",
          "uuid": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contacts[].createdAt` | date |  |
| `contacts[].email` | string |  |
| `contacts[].lastConversionDate` | date |  |
| `contacts[].links[].href` | string |  |
| `contacts[].name` | string |  |
| `contacts[].uuid` | string |  |

## Native endpoint

Through the native RD Station Marketing API, this operation is `GET /platform/segmentations/:id/contacts` (base URL `https://api.rd.services`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-segmentation-contacts.md) for the provider-specific parameters and requirements.

