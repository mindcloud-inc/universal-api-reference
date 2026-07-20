# Bedrijfsdata.nl: Lookup Company By KVK



```
GET https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/lookup-company-by-kvk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bedrijfsdata.nl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/lookup-company-by-kvk?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bedrijfsdatanl/latest/actions/lookup-company-by-kvk?${params}`, {
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
| `coc` | string | no | Optional Dutch Chamber of Commerce number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companies": [
        {
          "active": 1,
          "address": "string",
          "changedDate": "2026-05-07T12:00:00.000Z",
          "changedTime": "2026-05-07T12:00:00.000Z",
          "city": "string",
          "coc": "string",
          "description": "string",
          "entity": "string",
          "entityCode": "string",
          "id": "string",
          "name": "Ava Chen",
          "postcode": "string",
          "sbi": "string",
          "type": "string",
          "vestiging": "string"
        }
      ],
      "creditsUsed": 1,
      "found": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companies[].active` | number |  |
| `companies[].address` | string |  |
| `companies[].changedDate` | date |  |
| `companies[].changedTime` | date |  |
| `companies[].city` | string |  |
| `companies[].coc` | string |  |
| `companies[].description` | string |  |
| `companies[].entity` | string |  |
| `companies[].entityCode` | string |  |
| `companies[].id` | string |  |
| `companies[].name` | string |  |
| `companies[].postcode` | string |  |
| `companies[].sbi` | string |  |
| `companies[].type` | string |  |
| `companies[].vestiging` | string |  |
| `creditsUsed` | number |  |
| `found` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Bedrijfsdata.nl API, this operation is `GET /kvk` (base URL `https://fapi.bedrijfsdata.nl/v1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/lookup-company-by-kvk.md) for the provider-specific parameters and requirements.

