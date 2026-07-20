# Kintone: List Records

Retrieves records from Kintone.

```
GET https://connect.mindcloud.co/v1/universal/kintone/latest/actions/list-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kintone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kintone/latest/actions/list-records?connectionId=$CONNECTION_ID&appId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kintone/latest/actions/list-records?${params}`, {
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
| `appId` | number | yes | The Kintone app ID. |
| `query` | string | no | A Kintone query expression used to filter and sort records. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `totalCount` | boolean | no | Return the total count of matching records in addition to the record list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "records": [
        {}
      ],
      "totalCount": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `records` | array<object> | The matching Kintone records. |
| `totalCount` | string | The total number of matching records when requested. |

## Native endpoint

Through the native Kintone API, this operation is `GET /records.json` (base URL `{{credentials.baseUrl}}/k/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-records.md) for the provider-specific parameters and requirements.

