# Sempico Solutions SMS: Search Group Numbers



```
GET https://connect.mindcloud.co/v1/universal/sempicoSolutionsSMS/latest/actions/search-group-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sempico Solutions SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sempicoSolutionsSMS/latest/actions/search-group-numbers?connectionId=$CONNECTION_ID&id_group=1&numbers%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id_group": "1",
  "numbers[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sempicoSolutionsSMS/latest/actions/search-group-numbers?${params}`, {
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
| `id_group` | number | yes | Group ID to search. |
| `numbers[]` | array<string> | yes | Phone numbers to search for in the group. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "groupDetails": {
        "foundPhone": 1,
        "id_group": 1,
        "name_group": "Ava Chen"
      },
      "list": {
        "date_birth": "2026-05-07T12:00:00.000Z",
        "mcc": 1,
        "mnc": 1,
        "name": "Ava Chen",
        "phone": "string",
        "surname": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `groupDetails.foundPhone` | number | Number of matching phones found. |
| `groupDetails.id_group` | number | Group ID. |
| `groupDetails.name_group` | string | Group name. |
| `list` | array<object> | Matching phone records. |
| `list.date_birth` | date | Contact birth date. |
| `list.mcc` | number | Mobile country code. |
| `list.mnc` | number | Mobile network code. |
| `list.name` | string | Contact first name. |
| `list.phone` | string | Phone number. |
| `list.surname` | string | Contact surname. |

## Native endpoint

Through the native Sempico Solutions SMS API, this operation is `POST /group-number-search` (base URL `https://restapi.sempico.solutions/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-group-numbers.md) for the provider-specific parameters and requirements.

