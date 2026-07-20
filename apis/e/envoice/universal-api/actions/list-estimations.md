# Envoice: List Estimations

Retrieves estimations from Envoice.

```
GET https://connect.mindcloud.co/v1/universal/envoice/latest/actions/list-estimations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Envoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/envoice/latest/actions/list-estimations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/envoice/latest/actions/list-estimations?${params}`, {
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
| `page` | number | no | Result page number. |
| `pageSize` | number | no | Number of results per page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Count": 1,
      "ErrorMessages": [
        "string"
      ],
      "IsFaulted": true,
      "Result": [
        {}
      ],
      "TotalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Count` | number | Returned estimations count. |
| `ErrorMessages` | array<string> | Error messages. |
| `IsFaulted` | boolean | Whether the request faulted. |
| `Result` | array<object> | Estimation records. |
| `TotalCount` | number | Total estimations. |

## Native endpoint

Through the native Envoice API, this operation is `GET estimation/all` (base URL `https://www.envoice.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-estimations.md) for the provider-specific parameters and requirements.

